# 环境要求

## 1. 操作系统

!!! tip ""
    - 支持主流 Linux 发行版本（基于 Debian / RedHat）

| 操作系统   | 架构 | Linux 内核  | 软件要求       | 最小化硬件配置     |
| :------------ | :----------- | :------------ | :------------------------------------ | :-------------------- |
| linux/amd64   | x86_64       | >= 4.0    | wget curl tar gettext iptables python | 4Core/8GB RAM/60G HDD |
| linux/arm64   | aarch64      | >= 4.0    | wget curl tar gettext iptables python | 4Core/8GB RAM/60G HDD |
| linux/loong64 | loongarch64  | == 4.19   | wget curl tar gettext iptables python | 4Core/8GB RAM/60G HDD |

!!! tip ""
    Debian/Ubuntu
        ```sh
        apt-get update
        apt-get install -y wget curl tar gettext
        ```

    RedHat/CentOS
        ```sh
        yum update
        yum install -y wget curl tar gettext
        ```
## 2 中间件


| 名称    | 版本 | 默认字符集  | 默认字符编码  | TLS/SSL          |
| :------ | :------ | :--------------- | :----------------- | :--------------- |
| Postgresql   | >= 14  | utf8             | utf8_general_ci    | :material-check: |

| 名称    | 版本 | Sentinel         | Cluster            | TLS/SSL          |
| :------ | :------ | :--------------- | :----------------- | :--------------- |
| Hasura   | >= 2.27.0  | :material-check: | :material-close:   | :material-check: |

| 名称    | 版本 | Sentinel         | Cluster            | TLS/SSL          |
| :------ | :------ | :--------------- | :----------------- | :--------------- |
| Redis   | >= 6.0  | :material-check: | :material-close:   | :material-check: |

| 名称    | 版本 | Sentinel         | Cluster            | TLS/SSL          |
| :------ | :------ | :--------------- | :----------------- | :--------------- |
| nginx   | >= 1.14  | :material-check: | :material-close:   | :material-check: |

| 名称    | 版本 | Sentinel         | Cluster            | TLS/SSL          |
| :------ | :------ | :--------------- | :----------------- | :--------------- |
| minio   | >= 2022  | :material-check: | :material-close:   | :material-check: |

| 名称    | 版本 | Sentinel         | Cluster            | TLS/SSL          |
| :------ | :------ | :--------------- | :----------------- | :--------------- |
| zookeeper   | >= 3.4.6  | :material-check: | :material-close:   | :material-check: |

| 名称    | 版本 | Sentinel         | Cluster            | TLS/SSL          |
| :------ | :------ | :--------------- | :----------------- | :--------------- |
| kafka   | >= 2.13-2.8.1  | :material-check: | :material-close:   | :material-check: |

| 名称    | 版本 | Sentinel         | Cluster            | TLS/SSL          |
| :------ | :------ | :--------------- | :----------------- | :--------------- |
| keycloak   | >= 18.0.0  | :material-check: | :material-close:   | :material-check: |

| 名称    | 版本 | Sentinel         | Cluster            | TLS/SSL          |
| :------ | :------ | :--------------- | :----------------- | :--------------- |
| keycloak-mariadb   | >= 10.3.18  | :material-check: | :material-close:   | :material-check: |