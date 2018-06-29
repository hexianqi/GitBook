### Configure参数

* 标准选项参数：  
  `--help                   print this message                                   显示此帮助信息`

  `--log[=FILE|yes|no]      log tests and output to FILE [config.err]            记录测试并输出到config.err文件`

  `--prefix=PREFIX          install in PREFIX [/usr/local]                       安装程序到指定目录 [/usr/local]`

  `--libdir=DIR             install libs in DIR [PREFIX/lib]                     安装库到指定目录 [prefix/lib]`

  `--shlibdir=DIR           install shared libs in DIR [PREFIX/lib]              指定共享库路径 [prefix/lib]`

  `--incdir=DIR             install includes in DIR[PREFIX/include/ffmpeg]       指定包含路径 [prefix/include/ffmpeg]`

  `--mandir=DIR             install man page in DIR [PREFIX/man]                 指定手册路径 [prefix/man]`

  `--enable-mp3lame         enable MP3 encoding via libmp3lame[default=no]       启用mp3编码libmp3lame [关闭]`

  `--enable-libogg          enable Ogg support via libogg [default=no]           启用ogg支持libogg [关闭]`

  `--enable-vorbis          enable Vorbis support via libvorbis [default=no]     启用Vorbis支持libvorbis [关闭]`

  `--enable-faad            enable FAAD support via libfaad [default=no]         启用faad支持libfaad [关闭]`

  `--enable-faadbin         build FAAD support with runtime linking[default=no]  启用faad运行时链接支持 [关闭]`

  `--enable-faac            enable FAAC support via libfaac [default=no]         启用faac支持libfaac [关闭]`

  `--enable-libgsm          enable GSM support via libgsm [default=no]           启用GSM支持libgsm [关闭]`

  `--enable-xvid            enable XviD support via xvidcore [default=no]        启用xvid支持xvidcore [关闭]`

  `--enable-x264            enable H.264 encoding via x264 [default=no]          启用H.264编码 [关闭]`

  `--enable-mingw32         enable MinGW native/cross Windows compile            启用MinGW本地/交叉win环境编译`

  `--enable-mingwce         enable MinGW native/cross WinCE compile              启用MinGW本地/交叉winCE环境编译`

  `--enable-a52             enable GPLed A52 support [default=no]                启用A52支持 [关闭]`

  `--enable-a52bin          open liba52.so.0 at runtime [default=no]             启用运行时打开liba52.so.0 [关闭]`

  `--enable-dts             enable GPLed DTS support [default=no]                启用DTS支持 [关闭]`

  `--enable-pp              enable GPLed postprocessing support [default=no]     启用后加工支持 [关闭]`

  `--enable-static          build static libraries [default=yes]                 构建静态库 [启用]`

  `--disable-static         do not build static libraries [default=no]           禁止构建静态库 [关闭]`

  `--enable-shared          build shared libraries [default=no]                  构建共享库 [关闭]`

  `--disable-shared         do not build shared libraries [default=yes]          禁止构建共享库 [启用]`

  `--enable-amr_nb          enable amr_nb float audio codec                      启用amr_nb float音频编解码器`

  `--enable-amr_nb-fixed    use fixed point for amr-nb codec                     启用fixed amr_nb codec`

  `--enable-amr_wb          enable amr_wb float audio codec                      启用amr_wb float音频编解码器`

  `--enable-amr_if2         enable amr_wb IF2 audio codec                        启用amr_wb IF2音频编解码器`

  `--enable-sunmlib         use Sun medialib [default=no]                        启用Sun medialib [关闭]`

  `--enable-pthreads        use pthreads [default=no]                            启用pthreads [关闭]`

  `--enable-dc1394          enable IIDC-1394 grabbing using libdc1394 and libraw1394 [default=no] 启用libdc1394、libraw1394抓取IIDC-1394 [关闭]`

  `--enable-swscaler        software scaler support [default=no]                 启用软件定标器 [关闭]`

  `--enable-avisynth        allow reading AVISynth script files [default=no]     允许读取AVISynth脚本本件 [关闭]`

  `--enable-gpl             allow use of GPL code, the resulting libav* and ffmpeg will be under GPL [default=no]允许使用GPL（默认关闭）`

* 高级选项参数（供专业人员使用）：

 `--source-path=PATH       path to source code [/root/flv/ffmpeg]               源码的路径 [/root/flv/ffmpeg]`

`--cross-prefix=PREFIX    use PREFIX for compilation tools                     为编译工具指定路径`

`--cross-compile          assume a cross-compiler is used                      假定使用了交叉编译`

`--cc=CC                  use C compiler CC [gcc]                              指定使用何种C编译器 [gcc]`

`--make=MAKE              use specified make [make]                            使用特定的make`

`--extra-cflags=ECFLAGS   add ECFLAGS to CFLAGS []                             添加ECFLAGS到CFLAGS`

`--extra-ldflags=ELDFLAGS add ELDFLAGS to LDFLAGS [ -Wl,--as-needed]           添加ELDFLAGS到LDFLAGS [-Wl，--as-needed]`

`--extra-libs=ELIBS       add ELIBS []                                         添加ELIBS`

`--build-suffix=SUFFIX    suffix for application specific build []             为专用程序添加后缀`

`--arch=ARCH              select architecture [x86]                            选择机器架构 [x86]`

`--cpu=CPU                selects the minimum cpu required (affects instruction selection, may crash on older CPUs)    选用最低的cpu（影响指令的选择，可以在老CPU上出错） | `

`--powerpc-perf-enable    enable performance report on PPC (requires enabling PMC)                                     启用PPC上面的性能报告（需要启用PMC）`

`--disable-mmx            disable MMX usage                                    禁用MMX`

`--disable-armv5te        disable armv5te usage                                禁用armv5te`

`--disable-iwmmxt         disable iwmmxt usage                                 禁用iwmmxt`

`--disable-altivec        disable AltiVec usage                                禁用AltiVec`

`--disable-audio-oss      disable OSS audio support [default=no]               禁用OSS音频支持 [关闭]`

`--disable-audio-beos     disable BeOS audio support [default=no]              禁用BeOS音频支持 [关闭]`

`--disable-v4l            disable video4linux grabbing [default=no]            禁用video4linux提取 [关闭]`

`--disable-v4l2           disable video4linux2 grabbing [default=no]           禁用video4linux2提取 [关闭]`

`--disable-bktr           disable bktr video grabbing [default=no]             禁用bktr视频提取 [关闭]`

`--disable-dv1394         disable DV1394 grabbing [default=no]                 禁用DV1394提取 [关闭]`

`--disable-network        disable network support [default=no]                 禁用网络支持 [关闭]`

`--disable-ipv6           disable ipv6 support [default=no]                    禁用ipv6支持 [关闭]`

`--disable-zlib           disable zlib [default=no]                            禁用zlib [关闭]`

`--disable-simple_idct    disable simple IDCT routines [default=no]            禁用simple IDCT例程 [关闭]`

`--disable-vhook          disable video hooking support                        禁用video hooking支持`

`--enable-gprof           enable profiling with gprof [no]`

`--disable-debug          disable debugging symbols                            禁用调试符号`

`--disable-opts           disable compiler optimizations                       禁用编译器最优化`

`--disable-mpegaudio-hp   faster(but less accurate)MPEG audio decoding [default=no]启用更快的解码MPEG音频（但精确度较低）[关闭]`

`--disable-protocols      disable I/O protocols support [default=no]           禁用 I/O 协议支持 [关闭]`

`--disable-ffserver       disable ffserver build                               禁用生成ffserver`

`--disable-ffplay         disable ffplay build                                 禁用生成ffplay`

`--enable-small           optimize for size instead of speed                   启用优化文件尺寸大小（牺牲速度）`

`--enable-memalign-hack   emulate memalign, interferes with memory debuggers   启用模拟内存排列，由内存调试器干涉？`

`--disable-strip          disable stripping of executables and shared libraries禁用剥离可执行程序和共享库`

`--disable-encoder=NAME   disables encoder NAME                                禁用XX编码器`

`--enable-encoder=NAME    enables encoder NAME                                 启用XX编码器`

`--disable-decoder=NAME   disables decoder NAME                                禁用XX解码器`

`--enable-decoder=NAME    enables decoder NAME                                 启用XX解码器`

`--disable-encoders       disables all encoders                                禁用所有编码器`

`--disable-decoders       disables all decoders                                禁用所有解码器`

`--disable-muxer=NAME     disables muxer NAME                                  禁用XX混音器`

`--enable-muxer=NAME      enables muxer NAME                                   启用XX混音器`

`--disable-muxers         disables all muxers                                  禁用所有混音器`

`--disable-demuxer=NAME   disables demuxer NAME                                禁用XX解轨器`

`--enable-demuxer=NAME    enables demuxer NAME                                 启用XX解轨器`

`--disable-demuxers       disables all demuxers                                禁用所有解轨器`

`--enable-parser=NAME     enables parser NAME                                  启用XX剖析器`

`--disable-parser=NAME    disables parser NAME                                 禁用XX剖析器`

`--disable-parsers        disables all parsers                                 禁用所有剖析器`



