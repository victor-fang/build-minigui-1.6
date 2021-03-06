MinuGUI 代码不支持64位运行，已在Ubuntu 12.04 x86 版本上验证

1. Install toolchains
```
sudo apt-get install -y git gcc g++ binutils autoconf automake libtool make cmake \
    pkg-config libgtk2.0-dev libjpeg-dev libpng-dev libfreetype6-dev libsqlite3-dev libxml2-dev
```

2. Install QVFB

```
 $ sudo apt-get install qt4-dev-tools
```

3. Build libminigui-1.6.10

```
 $ tar -zxf libminigui-1.6.10.tar.gz
 $ cd libminigui-1.6.10
 $ ./configure
 $ make
 $ sudo make install
 $ cd ..
```

4. Install MiniGUI resources

```
$ tar -zxf minigui-res-1.6.10.tar.gz
$ cd minigui-res-1.6.10
$ sudo make install
$ cd ..
```

5. Build mGallery

```
$ git clone https://github.com/FMSoftCN/mgallery.git
$ ./autogen.sh
$ ./configure
$ make;
```

6. Run mGallery
Default all material files are stored in '/media' dirctory. Before run mgallery, you should create '/media' directory and its subdirectories: music, video, picture, recoder, ebook, cfg.

```
$ sudo mkdir /media
$ sudo mkdir /media/music /media/video /media/picture /media/ebook /media/recorder mkdir /media/cfg
```
Alternately you can define RES_TOP_DIR MACRO to set custom path.

```
$ qvfb -width 640 -height 480 &
$ cd /src
$ export LD_LIBRARY_PATH=/usr/local/lib:$LD_LIBRARY_PATH
$ ./startpmp
```
