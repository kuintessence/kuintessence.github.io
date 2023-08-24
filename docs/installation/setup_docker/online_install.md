# 平台安装
## 1 平台部署(docker-compose)
!!! tip ""
    - 支持主流 Linux 发行版本（基于 Debian / RedHat）
    - 需要安装[docker](https://docs.docker.com)、[docker-compose](https://docs.docker.com/compose/)

!!! tip "启动"
    <div class="termy">
    ```console
    // root@localhost:~#
    $ git clone https://github.com/nsccjn/kuintessence.git
    $ cd docker-compose
    $ docker-compose up -d
    ```
    </div>

!!! info "安装成功后，通过浏览器访问登录Kuintessence "
    ```sh
    地址: http://<Kuintessence服务器IP地址>:<服务运行端口>
    用户名: admin
    密码: admin
    ```

## 2 资源接入
### 准备工作
!!! tip ""
    - 准备一个HPC集群，集群需要Slurm或者PBS调度器。

!!! tip ""

    |   IP 地址     |    主机名       |    端口    | 操作系统         |  管理员用户    |    密码       |
    | ------------ | --------------- | ---------- | ---------------- |--- ---------- |--- ---------- |
    | 192.168.1.1  |     master      |     22     |     Centos 7     |      root     |   test123     ||

### 运行客户端Agent
!!! tip ""
    agent 目前只能是在 linux 机器上部署的集群队列调度器代理者，负责直接或通过 ssh 调用队列机器上的 Slurm 或者 PBS 以完
    成任务生命周期管理的程序。 agent 的配置文件遵从此文档 配置文件的配置会被环境变量所覆盖， docker-compose.yml 文件中
    有相关环境变量的配置
    <div class="termy">
    ```console
    // root@master:~#
    $ wget https://file.lab.supercomputing.link/s/NSNrRrd9b4EkjLk/download/agent.zip
    $ unzip agent.zip && cd ./agent
    ```
    </div> 
    修改config.yaml
    修改文件目录
    ```console
    // root@master:~#
    $ sed -i 's#/home/external/agent#/root/agent#g' ./config.yaml
    ```
    修改消息队列地址
    ```console
    // root@master:~#
    $ sed -i 's#192.168.10.1:50888#<Kafka服务器IP地址>:<Kafka服务运行端口>#g' ./config.yaml
    ```
    修改服务地址
    ```console
    // root@master:~#
    $ sed -i 's#https://example.com#http://<Kuintessence服务器IP地址>:<服务运行端口>>#g' ./config.yaml
    ```
    启动Agent
    ```console
    // root@master:~#
    $ chmod +x run-with-tumx.sh && ./run-with-tumx.sh
    ```
    检查Agent状态
    ```console
    // root@master:~#
    $ tmux  ls
    $ tmux attach -t agent_session 
    ```
