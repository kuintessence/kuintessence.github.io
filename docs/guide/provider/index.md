<p align="center"><font size=5>坤仪·万象-提供者门户</font></p>

:  坤仪·万象-提供者门户 (Kuintessence Provider) 是面向已经拥有高性能计算(HPC)集群的用户，提供 SAAS 化 HPC 管理服务的系统,它提供了队列接入，同时用户能方便的快速在业务系统内接入集群，满足 HPC 集群可用资源在线管理的需求,实现 HPC 管理的便捷化。

## 特性
!!! note ""

    - 🛠 简单易用性

        只需要接一个普通用户（非root），即可接入集群 

    - 🌐 高兼容性

        支持调用云原生调度系统，实现基于容器的作业提交；支持通过调用已有的 K8s 或 Docker 集群计算作业

    - 🚀 无侵入性

        只需提供一个集群普通用户，系统即可接入并调用集群资源，不会对原有集群作业、安全有任何影响

    - 🎯 开放性
        
        构建了一个开放的内容库，用户可以把自己的算例贡献出来，其他用户可以直接调用算例，而不需要学习这个软件的命令、参数


## 使用

1.克隆仓库

```bash
git clone https://github.com/nsccjn/kuintessence-provider.git
```

2.打开 [Kuintessence](../server/index.md) 启动.