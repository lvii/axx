🚀️
🌕️
🌞️
🍺️
🐳
🐠
🐟
🐡
🐬
🐋
🦈
🦆
🦅
🦉
🐓
🦃
🐌
🐌
🐌
-------------
Actions-OpenWrt — 多设备固件自动云编译 [![](https://img.shields.io/badge/-云编译固件-green.svg)](#云编译固件-)
======================
关于第三方全家桶软件仓库更新的说明 [![](https://img.shields.io/badge/-软件库更新说明-green.svg)](#软件库更新说明-)
-------------
- 固件来源：
[![Lean](https://img.shields.io/badge/Lede-Lean-red.svg?style=flat&logo=appveyor)](https://github.com/coolsnowwolf/lede) 
 [![Lienol](https://img.shields.io/badge/Package-Lienol-blueviolet.svg?style=flat&logo=appveyor)](https://github.com/Lienol/openwrt-package)  [![CTCGFW](https://img.shields.io/badge/OpenWrt-CTCGFW-orange.svg?style=flat&logo=appveyor)](https://github.com/project-openwrt/openwrt) [![joyblablabla](https://img.shields.io/badge/Mod-Joecaicai-success.svg?style=flat&logo=appveyor)](https://github.com/Joecaicai/Actions-OpenWrt/actions)
- 每日两次自动拉取更新所有上游源码至上方软件仓库，所以此软件仓库永远都是最新的。
- 云编译脚本会调用此仓库软件编译OpenWrt固件，每日一次编译。
- 默认源编译的固件特别说明： 管理地址默认IP：10.0.0.1 登陆密码：默认password WIFI密码：gds.2021
- Boos4721源编译的固件特别说明： 管理地址默认IP：10.10.10.1 登陆密码：默认boos WIFI密码：1234567890
-------------
温馨提示
-------------
- 5.10和5.15内核：猫咪科学学习，配置文件订阅下：有个使用规则集，请关闭这个。因为此规则集有问题会导致断网或无网络。

- 支持的设备平台以及固件下载地址 [![](https://img.shields.io/badge/-设备及固件列表下载-green.svg)](#设备及固件列表下载-)

|    序号   |     平台+设备名称     |   编译状态+下载链接 |  
| :-----------------: | :-------------: |:-----------------: | 
| 1 |  [![](https://img.shields.io/badge/OpenWrt-MI--R4A-green.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/MI-R4A.yml)| [![MI-R4A](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/MI-R4A.yml/badge.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/MI-R4A.yml)|
| 2 |  [![](https://img.shields.io/badge/OpenWrt-MI--mini-green.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/MI-mini.yml)| [![MI-mini](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/MI-mini.yml/badge.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/MI-mini.yml)|
| 3 |  [![](https://img.shields.io/badge/OpenWrt-MI--CR660X-green.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/MI-CR660X.yml)| [![MI-CR660X](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/MI-CR660X.yml/badge.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/MI-CR660X.yml)|
| 4 |  [![](https://img.shields.io/badge/OpenWrt-5.15--AX6-green.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/5.15-AX6.yml)| [![5.15-AX6](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/5.15-AX6.yml/badge.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/5.15-AX6.yml)|
| 5 |  [![](https://img.shields.io/badge/OpenWrt-5.15--AX6S-green.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/5.15-AX6S.yml)| [![5.15-AX6S](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/5.15-AX6S.yml/badge.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/5.15-AX6S.yml)|
| 6 |  [![](https://img.shields.io/badge/OpenWrt-5.15--purple-AX6.yml-green.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/5.15-purple-AX6.yml)| [![5.15-purple-AX6](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/5.15-purple-AX6.yml/badge.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/5.15-purple-AX6.yml)|
| 7 |  [![](https://img.shields.io/badge/OpenWrt-AX6--Almighty-green.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/AX6-Almighty.yml)| [![Almighty-AX6](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/Almighty-AX6.yml/badge.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/Almighty-AX6.yml)|
| 8 |  [![](https://img.shields.io/badge/OpenWrt-5.15--AX3600-green.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/5.15-AX3600.yml)| [![5.15-AX3600](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/5.15-AX3600.yml/badge.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/5.15-AX3600.yml)|
| 9 |  [![](https://img.shields.io/badge/OpenWrt-Almighty--AX3600-green.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/5.15-AX3600.yml)| [![Almighty-AX3600](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/Almighty-AX3600.yml/badge.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/Almighty-AX3600.yml)|
| 10 |  [![](https://img.shields.io/badge/OpenWrt-5.15--AX9000-green.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/5.15-AX9000.yml)| [![5.15-AX9000](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/5.15-AX9000.yml/badge.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/5.15-AX9000.yml)|
| 11 |  [![](https://img.shields.io/badge/OpenWrt-Almighty--AX9000-green.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/Almighty-AX9000.yml)| [![Almighty-AX9000](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/Almighty-AX9000.yml/badge.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/Almighty-AX9000.yml)|
| 12 |  [![](https://img.shields.io/badge/OpenWrt-nonss--ax6/ax3600-green.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/no-nss-ax6-ax3600.yml)| [![no-nss-ax6-ax3600](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/no-nss-ax6-ax3600.yml/badge.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/no-nss-ax6-ax3600.yml)|
| 13 |  [![](https://img.shields.io/badge/OpenWrt-HiWiFi--HC5962-green.svg)](https://github.com/Joecaicai/Actions-OpenWrt/actions/workflows/HIWIFI-HC5962.yml)| [![HIWIFI-HC5962](https://github.com/Joecaicai/AutoBuild-OpenWrt/actions/workflows/HIWIFI-HC5962.yml/badge.svg)](https://github.com/Joecaicai/AutoBuild-OpenWrt/actions/workflows/HIWIFI-HC5962.yml)|
| 14 |  [![](https://img.shields.io/badge/OpenWrt-X86--64-green.svg)](https://github.com/Joecaicai/AutoBuild-OpenWrt/actions/workflows/X86-64.yml)| [![X86-64](https://github.com/Joecaicai/AutoBuild-OpenWrt/actions/workflows/X86-64.yml/badge.svg)](https://github.com/Joecaicai/AutoBuild-OpenWrt/actions/workflows/X86-64_.yml)|

关于自动编译固件的说明 [![](https://img.shields.io/badge/-自动编译说明-green.svg)](#自动编译说明-)
-------------

- 每日自动编译，自动拉取最新版本插件。
- 自用固件仅包含 （pw,S,上网时间控制，upnp,ddns,去广告，多拨，负载均衡，流量监控，主题只加入了jerrykuku的18.06 luci-theme-argon以及infinityfreedom等主题）

-------------
手动编译
======================
1. 首先装好 Linux 系统，推荐 Debian 11 或 Ubuntu LTS  
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

   ```bash
   sudo apt update -y
   sudo apt full-upgrade -y
   sudo apt install -y ack antlr3 asciidoc autoconf automake autopoint binutils bison build-essential \
   bzip2 ccache cmake cpio curl device-tree-compiler fastjar flex gawk gettext gcc-multilib g++-multilib \
   git gperf haveged help2man intltool libc6-dev-i386 libelf-dev libglib2.0-dev libgmp3-dev libltdl-dev \
   libmpc-dev libmpfr-dev libncurses5-dev libncursesw5-dev libreadline-dev libssl-dev libtool lrzsz \
   mkisofs msmtp nano ninja-build p7zip p7zip-full patch pkgconf python2.7 python3 python3-pip qemu-utils \
   rsync scons squashfs-tools subversion swig texinfo uglifyjs upx-ucl unzip vim wget xmlto xxd zlib1g-dev
   ```

以下的命令适用Ubuntu 20
-------------

   ```bash
   sudo apt update -y
   sudo apt full-upgrade -y
   sudo apt install -y ack antlr3 asciidoc autoconf automake autopoint binutils bison build-essential \
   bzip2 ccache cmake cpio curl device-tree-compiler fastjar flex gawk gettext gcc-multilib g++-multilib \
   git gperf haveged help2man intltool libc6-dev-i386 libelf-dev libglib2.0-dev libgmp3-dev libltdl-dev \
   libmpc-dev libmpfr-dev libncurses5-dev libncursesw5-dev libreadline-dev libssl-dev libtool lrzsz \
   mkisofs msmtp nano ninja-build p7zip p7zip-full patch pkgconf python2.7 python3 python3-pip qemu-utils \
   rsync scons squashfs-tools subversion swig texinfo uglifyjs upx-ucl unzip vim wget xmlto xxd zlib1g-dev
   ```
   
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

-------------
## SSH-Actions

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

[MIT](https://github.com/MuaCat/Actions-OpenWrt/blob/master/LICENSE) © P3TERX

