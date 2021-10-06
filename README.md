![GitHub Repo stars](https://img.shields.io/github/stars/8kChow/Actions-OpenWrt?color=Blue&label=Stars&style=for-the-badge)
![GitHub forks](https://img.shields.io/github/forks/8kChow/Actions-OpenWrt?color=Blue&label=Fork&style=for-the-badge)
![GitHub](https://img.shields.io/github/license/8kChow/Actions-OpenWrt?color=Blue&style=for-the-badge)


-- 关于第三方全家桶软件仓库更新的说明 [![](https://img.shields.io/badge/-软件库更新说明-green.svg)](#软件库更新说明-)
-------------

- 每日两次自动拉取更新所有上游源码至上方软件仓库，所以此软件仓库永远都是最新的。
- 云编译脚本会调用此仓库软件编译OpenWrt固件，每日一次编译。

Actions-OpenWrt — 多设备固件自动云编译 [![](https://img.shields.io/badge/-云编译固件-green.svg)](#云编译固件-)
======================
默认IP： 10.0.0.1  默认无密码或者： password
-------------
-- 支持的设备平台以及固件下载地址 [![](https://img.shields.io/badge/-设备及固件列表下载-green.svg)](#设备及固件列表下载-)
-------------

|    序号   |     平台+设备名称     |   编译状态+下载链接 |  
| :-----------------: | :-------------: |:-----------------: | 
| 1 |   [![](https://img.shields.io/badge/OpenWrt-x86--64-green.svg)](https://github.com/MuaCat/Actions-OpenWrt/actions/workflows/x86_64.yml) | [![X86_64](https://github.com/MuaCat/Actions-OpenWrt/actions/workflows/X86_64.yml/badge.svg)](https://github.com/MuaCat/Actions-OpenWrt/actions/workflows/X86_64.yml)  |
| 2 |   [![](https://img.shields.io/badge/OpenWrt-HiWiFi--HC5962-green.svg)](https://github.com/MuaCat/Actions-OpenWrt/actions/workflows/hc5962.yml) | [![HIWIFI_HC5962](https://github.com/MuaCat/Actions-OpenWrt/actions/workflows/HIWIFI_HC5962.yml/badge.svg)](https://github.com/MuaCat/Actions-OpenWrt/actions/workflows/HIWIFI_HC5962.yml) |
| 3 |   [![](https://img.shields.io/badge/OpenWrt-RedMi--AC2100-green.svg)](https://github.com/MuaCat/Actions-OpenWrt/actions/workflows/mi_ax3600.yml) | [![RedMi_AC2100](https://github.com/MuaCat/Actions-OpenWrt/actions/workflows/RedMi_AC2100.yml/badge.svg)](https://github.com/MuaCat/Actions-OpenWrt/actions/workflows/RedMi_AC2100.yml) |
| 4 |   [![](https://img.shields.io/badge/OpenWrt-XIAOMI--AX3600-green.svg)](https://github.com/MuaCat/Actions-OpenWrt/actions/workflows/mi_ax3600.yml) | [![XIAOMi_AX3600](https://github.com/MuaCat/Actions-OpenWrt/actions/workflows/XIAOMi_AX3600.yml/badge.svg)](https://github.com/MuaCat/Actions-OpenWrt/actions/workflows/XIAOMi_AX3600.yml) |

-- 关于自动编译固件的说明 [![](https://img.shields.io/badge/-自动编译说明-green.svg)](#自动编译说明-)
-------------

- 每日自动编译，自动拉取最新版本插件。
- 自用固件仅包含 （pw,S,上网时间控制，upnp,ddns,去广告，多拨，负载均衡，流量监控，主题只加入了jerrykuku的18.06 luci-theme-argon以及infinityfreedom等主题）

手动编译
======================
1. 首先装好 Ubuntu 64bit，推荐  Ubuntu  18 LTS x64  
2. 命令行输入

```bash
sudo apt-get update
```
然后输入命令搭建系统环境
-------------
**如果你使用`root`执行了以上命令，那从此时开始，你必须使用`非root`权限用户进行后续操作**
-------------
以下的命令适用Ubuntu 18
-------------
>sudo apt-get -y install build-essential asciidoc binutils bzip2 gawk gettext git libncurses5-dev patch python3 python2.7 unzip zlib1g-dev lib32gcc1 libc6-dev-i386 subversion flex node-uglify git gcc-multilib p7zip p7zip-full msmtp libssl-dev texinfo libglib2.0-dev xmlto qemu-utils upx-ucl libelf-dev autoconf automake libtool autopoint device-tree-compiler g++-multilib antlr3 gperf wget curl swig rsync

以下的命令适用Ubuntu 20
-------------
>sudo apt-get -y install build-essential asciidoc binutils bzip2 gawk gettext git libncurses5-dev libz-dev patch python3 python2.7 unzip zlib1g-dev lib32gcc1 libc6-dev-i386 subversion flex uglifyjs git-core gcc-multilib p7zip p7zip-full msmtp libssl-dev texinfo libglib2.0-dev xmlto qemu-utils upx libelf-dev autoconf automake libtool autopoint device-tree-compiler g++-multilib antlr3 gperf wget curl swig rsync

3. 使用 `git clone https://github.com/coolsnowwolf/lede` 命令下载好源代码，然后 `cd lede` 进入目录

4. `make -j8 download V=s` 下载dl库（国内请尽量全局科学上网）

5. 输入 `make -j1 V=s` （-j1 后面是线程数。第一次编译推荐用单线程）即可开始编译你要的固件了。

本套代码保证肯定可以编译成功。里面包括了 R21 所有源代码，包括 IPK 的。

你可以自由使用，但源码编译二次发布请注明我的 GitHub 仓库链接。谢谢合作！
=

二次编译：
```bash
cd lede
git pull
./scripts/feeds update -a && ./scripts/feeds install -a
make defconfig
make -j8 download
make -j$(($(nproc) + 1)) V=s
```

如果需要重新配置：
```bash
rm -rf ./tmp && rm -rf .config
make menuconfig
make -j$(($(nproc) + 1)) V=s
```

编译完成后输出路径：bin/targets

## 2.Actions

同意工作流，然后开整。

![](https://gitee.com/Unkaer/blog/raw/master/images/material/20210307205947.webp)

等到 ssh连接 界面
![](https://gitee.com/Unkaer/blog/raw/master/images/material/20210307210916.webp)

单击 `url` 进行访问;
![](https://gitee.com/Unkaer/blog/raw/master/images/material/20210307210937.webp)

黑屏 按 `Ctrl`+`C`变为命令行模式 ;
输入 `cd openwrt/ && make menuconfig` 进入菜单

```
cd openwrt/ && make menuconfig
```

![](https://gitee.com/Unkaer/blog/raw/master/images/material/20210307211012.webp)
![](https://gitee.com/Unkaer/blog/raw/master/images/material/20210307211148.webp)

### 2.1设置插件
插件对照参考 [OpenWrt 编译 LuCI -> Applications 添加插件应用说明-L大](https://www.right.com.cn/forum/thread-3682029-1-1.html)
`Y` 确定选中 `N`取消选中

#### 2.1.1 机型选择
前三个是设置机型，默认已经选好了 小米R4A千兆版
![机型](https://user-images.githubusercontent.com/45261780/128300236-881f51d1-6475-4621-83f4-61775e01030e.png)

#### 2.1.2 主题选择
在 `LuCI` --> `Themes` 中进行设置
![LuCI](https://user-images.githubusercontent.com/45261780/128300627-a3af1f69-2c2f-49fa-86ce-8da6b3a0d0d4.png)

#### 2.1.3 插件选择
在 `LCTY` --> `Applications` 中进行设置
![Applications](https://user-images.githubusercontent.com/45261780/128300725-26799ad1-1bbb-4035-8ff0-aeaba1635dd3.png)

#### 2.1.4 保存设置
方向键移动选中 `Save` 回车确认
![1](https://user-images.githubusercontent.com/45261780/128300983-93ee554e-e72d-4082-8550-265ff087971e.png)
保存为 默认的文件名
![2](https://user-images.githubusercontent.com/45261780/128301040-705307f5-2b0b-42d0-b52c-5608807ebcd5.png)

或者 连按两下 `ESC` 返回至退出菜单界面，
会弹出确认是否保存菜单，确认即可
![3](https://user-images.githubusercontent.com/45261780/128301176-8f163e5e-84f3-4700-ba38-7732f4fe16f4.png)


### 2.2下载本次修改的配置文件（可选）
下次升级就可以直接用，不必再 ssh 选择插件了

```
rm -f .config.old && make defconfig && ./scripts/diffconfig.sh > seed.config && cat seed.config
```

*自己复制保存到合适的位置
*在手动修改成项目的 .config 文件

### 2.3退出 ssh
在命令行界面 `ctrl`+`D`  退出 ssh
![批注 2021-08-05 115225](https://user-images.githubusercontent.com/45261780/128301252-f054fa0a-6544-4770-8e99-217946f9b692.png)
![批注 2021-08-05 115238](https://user-images.githubusercontent.com/45261780/128301319-5b6969b1-94e5-43f7-97c7-6f69acbd92ec.png)


特别提示：
------
源代码中绝不含任何后门和可以监控或者劫持你的 HTTPS 的闭源软件， SSL 安全是互联网最后的壁垒。安全干净才是固件应该做到的；

[MIT](https://github.com/P3TERX/Actions-OpenWrt/blob/main/LICENSE) © P3TERX
