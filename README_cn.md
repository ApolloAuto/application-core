# Apollo Core Workspace

Apollob包管理开发调试样例工程，使用方法参考[包管理安装方式](https://apollo.baidu.com/community/Apollo-Homepage-Document?doc=BYFxAcGcC4HpYIbgPYBtXIHQCMEEsATAV0wGNkBbWA5UyRFdZWVBEAU0hFgoIH0adPgCY%2BADwCiAVnEBBCeIAcATnETFcgMxKZkgGxKAwkoDsa3YoAi45WdGSLxsYt0SzY%2BXICMa98oAMSgYALF7%2B2NhemsLBJsrCYZqKwors7AikBIp6miYmpFJSXpigFKhAA)

### 文件目录组织

```shell
.
├── core              # 依赖包配置，包括apollo核心包，以及一些工具包
├── profiles          # 整车应用配置，以单lidar、双camera车型为例
├── kill_all.sh       # 停止所有apollo相关进程
└── WORKSPACE         # bazel 的配置
```

## 安装步骤

请在`git clone`后执行以下命令：
```shell
# 启动容器
aem start

# 进入容器
aem enter

# 安装软件包
buildtool build

# 下载地图（此处下载sunnyvale，如果需要其他地图，可以用buildtool map list查看可供下载的地图）
buildtool map get sunnyvale

# 切换车辆配置 (您可以参考profiles目录下的sample编写自己的profile配置)
aem profile use sample

# 启动Dreamview+
aem bootstrap restart --plus
```
