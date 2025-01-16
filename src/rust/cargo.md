# Cargo


## 配置crates.io镜像

> 配置文件目录: ~/.cargo/config.toml

```toml

[source.crates-io]
replace-with = 'aliyun'
[source.aliyun]
registry = "sparse+https://mirrors.aliyun.com/crates.io-index/"

```
