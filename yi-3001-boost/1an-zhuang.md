### 1、下载boost库

    下载地址：http://www.boost.org/users/download/ 

### 2、配置编译环境

*     先安装gcc编译器。
*     在windwos的环境变量中添加gcc.exe可执行文件的环境变量，这样在任何目录下都可以使用gcc命令。

### 3、生成编译工具

1. Win+R-&gt;输出cmd，以管理员身份打开windows的命令行界面， 进入boost\_1\_66\_0文件的目录， 执行命令bootstrap gcc，等待一分钟左右就会生成两个可执行文件bjam.exe和b2.exe；
2. Win+R-&gt;输出cmd，以管理员身份打开windows的命令行界面， 进入boost\_1\_66\_0\tools\build\v2\engine文件的目录，执行命令build mingw命令， 执行完以后， 将会生成一个用于编译boost c++库的bjam.exe和b2.exe的程序，复制到boost\_1\_66\_0文件的目录；

### 4、编译

   执行下面的编译命令bjam.exe –build-type=complete toolset=gcc stage variant=release link=shared threading=multi runtime-link=shared 

| 参数名 | 解释 |
| :---: | :--- |
| stage/install | stage表示只生成库（dll和lib），install还会生成包含头文件的include目录。推荐使用stage，因为install生成的这个include目录实际就是boost安装包解压缩后的boost目录（D:\SDK\boost\_1\_66\_0\boost，只比include目录多几个非hpp文件，都很小），所以可以直接使用，而且不同的IDE都可以使用同一套头文件，这样既节省编译时间，也节省硬盘空间。 |
| --stagedir | 配合stage时使用，指定编译生成文件的路径。默认路径为当前路径下的"./stage"文件夹。 |
| --prefix  | 配合install时使用，指定编译生成文件的路径。在Win32默认为"C:\Boost"；在Unix/Linux上默认为"/usr/local"。推荐给不同的IDE指定不同的目录，如VS2010对应的是D:\SDK\boost\_1\_66\_0\vc10\lib，否则都生成到一个目录下面，难以管理。如果使用了install参数，那么还将生成头文件目录，vc10对应的就是D:\SDK\boost\_1\_66\_0\vc10\include\boost-1\_50\boost。 |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |





