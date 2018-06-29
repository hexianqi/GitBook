### 1、下载boost库

    官方下载地址：[http://www.boost.org/users/download](http://www.boost.org/users/download)

### 2、配置编译环境

* 先安装gcc编译器。
* 在windwos的环境变量中添加gcc.exe可执行文件的环境变量，这样在任何目录下都可以使用gcc命令。

### 3、生成编译工具

1. Win+R-&gt;输出cmd，以管理员身份打开windows的命令行界面， 进入boost\_1\_66\_0文件的目录， 执行命令bootstrap gcc，等待一分钟左右就会生成两个可执行文件bjam.exe和b2.exe；
2. Win+R-&gt;输出cmd，以管理员身份打开windows的命令行界面， 进入boost\_1\_66\_0\tools\build\v2\engine文件的目录，执行命令build mingw命令， 执行完以后， 将会生成一个用于编译boost c++库的bjam.exe和b2.exe的程序，复制到boost\_1\_66\_0文件的目录；

### 4、编译

    执行下面的编译命令bjam.exe –build-type=complete toolset=gcc stage variant=release link=shared threading=multi runtime-link=shared

| 参数名 | 解释 |
| :--- | :--- |
| stage/install | stage表示只生成库（dll和lib），install还会生成包含头文件的include目录。推荐使用stage，因为install生成的这个include目录实际就是boost安装包解压缩后的boost目录（D:\SDK\boost\_1\_66\_0\boost，只比include目录多几个非hpp文件，都很小），所以可以直接使用，而且不同的IDE都可以使用同一套头文件，这样既节省编译时间，也节省硬盘空间。 |
| --stagedir | 配合stage时使用，指定编译生成文件的路径。默认路径为当前路径下的"./stage"文件夹。 |
| --prefix | 配合install时使用，指定编译生成文件的路径。在Win32默认为"C:\Boost"；在Unix/Linux上默认为"/usr/local"。推荐给不同的IDE指定不同的目录，如VS2010对应的是D:\SDK\boost\_1\_66\_0\vc10\lib，否则都生成到一个目录下面，难以管理。如果使用了install参数，那么还将生成头文件目录，vc10对应的就是D:\SDK\boost\_1\_66\_0\vc10\include\boost-1\_50\boost。 |
| --exec-prefix=&lt;EPREFIX&gt; | 安装体系结构所依赖的文件。 |
| --libdir=&lt;DIR&gt; | 指定库文件安装目录。 |
| --includedir=&lt;HDRDIR&gt; | 指定头文件安装目录。 |
| --with-&lt;library&gt;/ --without-&lt;library&gt; | 选择编译/不编译哪些库。本人不需要编译python库，所以排除之，可以根据各人需要选择，默认是全部编译。注意：如果选择编译python的话，是需要python语言支持的，应该到python[官方主页](http://www.python.org)下载安装。 |
| --help | 显示帮助信息。 |
| --build-dir=DIR | 编译生成的中间文件的路径。默认就在根目录（D:\SDK\boost\_1\_50\_0）下，目录名为bin.v2，等编译完成后可将这个目录全部删除（没用了），所以不需要去设置。 |
| --show-libraries | 显示需要编译才能使用的Boost库列表。 |
| toolset | 指定编译器，可选的如borland、gcc、msvc（VC6）、msvc-10.0（VS2010）等。 |
| link=static\|shared | 生成动态链接库/静态链接库。生成动态链接库需使用shared方式，生成静态链接库需使用static方式。注意：static方式下，最终生成的很多静态链接库大小都在几兆、几十兆，甚至接近百兆。这么大的库我们一般是不会采用静态链接方式的，所以这些库不推荐以static方式编译（without掉）；如果已经编译了赶快删，肯定没用，否则将占用近1G的硬盘空间。以下是巨型库黑名单：wave、graph、math、regex、test、program\_options、serialization、signals。 |
| runtime-link=static\|shared | 动态/静态链接C/C++运行时库。同样有shared和static两种方式，这样runtime-link和link一共可以产生4种组合方式。虽然它和link属性没有直接关系，但我们习惯上，一个工程如果用动态链接那么所有库都用动态链接，如果用静态链接那么所有库都用静态链接。所以这样其实只需要编译2种组合即可，即link=shared runtime-link=shared和link=static runtime-link=static。 |
| threading=single\|multi | 单/多线程编译。一般都写多线程程序，当然要指定multi方式了；如果需要编写单线程程序，那么还需要编译单线程库，可以使用single方式。 |
| variant=debug\|release | 编译debug/release版本。一般都是程序的debug版本对应库的debug版本，所以两个都编译。 |



