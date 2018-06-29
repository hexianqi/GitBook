### 1.安装

* Msys2[官网](http://http://www.msys2.org/)下载；
* 增加中国科学技术开源软件镜像地址：
  分别在msys64/etc/pacman.d路径下的mirrorlist.msys、mirrorlist.mingw32、mirrorlist.mingw64文件的地址开头添加：

`#mirrorlist.msys`

`Server = http://mirrors.ustc.edu.cn/msys2/msys/$arch/`

`#mirrorlist.mingw32`

`Server = http://mirrors.ustc.edu.cn/msys2/mingw/i686/`

`#mirrorlist.mingw64`

`Server = http://mirrors.ustc.edu.cn/msys2/mingw/x86_64/`

* 安装Msys2后，第一次运行下msys2\_shell.cmd，提示第一次设置初始化完毕后，就可以运行Msys2.exe、mingw64.exe或mingw32.exe，主要区别：
  * mingw32 优先使用 msys64/mingw32 下的工具；
  * mingw64 优先使用 msys64/mingw64 下的工具；
  * msys2 两个都不使用，只用自身 msys 的工具；

### 2.升级

一般第一次打开msys2用“pacman -Syu”全面升级，然后会提示关闭终端，再次打开后再一次运行”pacman -Syu”。若是不想升级可以直接用pacman安装自需要的软件，如vim，git，gcc\(即MinGw\)等。

### 3.pacman

| pacman -S &lt;packge-name&gt; | 安装软件 |
| :--- | :--- |
| pacman -U &lt;gz-file&gt; | 安装本地包，其扩展名为 pkg.tar.gz |
| pacman -Syu | 同步Msys2源，并更新 |
| pacman -Sy | 仅同步源 |
| pacman -Su | 更新系统 |
| pacman -Sy &lt;packge-name&gt; | 同步源后再安装软件 |
| pacman -R &lt;packge-name&gt; | 该命令将只删除包，不包含该包的依赖。 |
| pacman -Rs &lt;packge-name&gt; | 在删除包的同时，也将删除其依赖。 |
| pacman -Rd &lt;packge-name&gt; | 在删除包时不检查依赖。 |
| pacman -Ss &lt;keywords&gt; | 这将搜索含关键字的包。 |
| pacman -Qi &lt;packge-name&gt; | 查看有关包的信息。 |

### 4.安装工具

* Vim：pacman -S vim     \# 安装完后在Msys2的~/下touch一个.vimrc，里面加入设置：set bs=2，不然vim在插入模式下的退格不能用。
* 32位MinGW-w64：pacman -S  mingw-w64-i686-toolchain

* 64位MinGW-w64：pacman -S  mingw-w64-x86\_64-toolchain

* Qt5：pacman -S  mingw-w64-x86\\_64-qt5 mingw-w64-x86\\_64-qt-creato

* 其他常用工具：pacman -S  base-devel  git  mercurial  cvs  wget  p7zip  perl  ruby  python2

### 5.编译一般开源代码（qt使用最好用32位的，64位不一定能编译过）

* 用CD命令进入源码目录
* ./configure \[--prefix=/test // 加编译目录\] \[--enable-shared // 启用动态库\] 
* make 或 mingw32-make
* make install



