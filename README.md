Welcome to Lean's  git source of OpenWrt and packages

中文：如何编译自己需要的 OpenWrt 固件

注意：
1. 不要用 root 用户 git 和编译！！！
2. 国内用户编译前最好准备好梯子
3. 默认登陆IP 192.168.1.1, 密码 password

编译命令如下:

1. 首先装好 Ubuntu 64bit，推荐  Ubuntu  14 LTS x64

2. 命令行输入 sudo apt-get update ，然后输入
sudo apt-get -y install build-essential asciidoc binutils bzip2 gawk gettext git libncurses5-dev libz-dev patch unzip zlib1g-dev lib32gcc1 libc6-dev-i386 subversion flex uglifyjs git-core gcc-multilib p7zip p7zip-full msmtp libssl-dev texinfo libglib2.0-dev xmlto qemu-utils upx libelf-dev autoconf automake libtool autopoint device-tree-compiler

3. git clone https://github.com/coolsnowwolf/lede 命令下载好源代码，然后 cd lede 进入目录

4. ./scripts/feeds update -a 
   ./scripts/feeds install -a
   make menuconfig 

5. 最后选好你要的路由，输入 make -j1 V=s （-j1 后面是线程数。第一次编译推荐用单线程，国内请尽量全局科学上网）即可开始编译你要的固件了。

本套代码保证肯定可以编译成功。里面包括了 R9 所有源代码，包括 IPK 的。

你可以自由使用，但源码编译二次发布请注明我的 GitHub 仓库链接。谢谢合作！



# AutoBuild-OpenWrt

Build OpenWrt firware [Lean's OpenWrt](https://github.com/coolsnowwolf/lede) using GitHub Actions  
Hereby thank P3TERX for his amazing job: https://github.com/P3TERX/Actions-OpenWrt/

## Usage

- Sign up for [GitHub Actions](https://github.com/features/actions/signup)
- Fork [this GitHub repository](https://github.com/esirplayground/AutoBuild-OpenWrt)
- Click [.github/workflows] folder on the top of repo and you could see two workflow files, one's for x86 32bit and the other's for x86_64.
- Edit the workflow file you desire，uncomment push section 3 lines together and submit the commit.(Other 2 methods wait you to discover)
- The build starts automatically. Progress can be viewed on the Actions page.
- When the build is complete, click the `Artifacts` button in the upper right corner of the Actions page to download the binaries.

[For the details please visit my Y2B Channel (in Chinese) | 视频教程](https://www.youtube.com/c/esirplayground)
