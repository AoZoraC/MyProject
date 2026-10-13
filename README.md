# MyProject

个人项目仓库。

## 说明

本仓库由 `D:\tool\Code\Git` 初始化，远程地址：<https://github.com/AoZoraC/MyProject.git>

## 本地特殊配置

本机装有 SteamTools（Watt Toolkit）网络加速工具，它会以中间人方式代理 GitHub 流量。
因此本仓库使用 OpenSSL 后端 + 合并了本机根证书的 CA 包，相关配置仅作用于本仓库
（`.git/config`），不会影响其他项目：

```
http.sslBackend = openssl
http.sslCAInfo  = D:/tool/Code/Git/.certs/ca-bundle-with-steamtools.crt
```

其中 `.certs/` 目录已加入 `.gitignore`，不会提交到远程。
