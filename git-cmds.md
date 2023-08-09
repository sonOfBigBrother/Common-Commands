### 下载 Github 仓库超时问题

由于国内特殊网络环境问题，时长会遇到下载项目超时的问题，个人使用的代理工具主要还是Clash，只要为***git***工具设置代理即可

```bash
# 全局配置代理
git config --global http.proxy http://127.0.0.1:7890

# 取消全局代理
git config --global --unset http.proxy
```

### 不同系统使用不同换行符导致的更新问题

由于`unix/linux`系统和`windows`系统采用不同的形式表示换行符，给跨平台协作开发代码时带来麻烦，Git 工具提供了一个`autocrlf`的配置项，该配置有三个可选项：

- `true` 表示提交时转换为 LF，检出时转换 CRLF ；
- `input` 表示提交时转换为 LF，检出时不转换；
- `false` 表示不做转换。

```bash
git config --global core.autocrlf true
```

### 查看所有的配置信息

```bash
git config --list
```

