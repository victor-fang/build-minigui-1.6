Ubuntu 12.04

1. Install toolchains
sudo apt-get install -y git gcc g++ binutils autoconf automake libtool make cmake pkg-config libgtk2.0-dev libjpeg-dev libpng-dev libfreetype6-dev libsqlite3-dev libxml2-dev

2. Install QVFB

```
 $ sudo apt-get install qt4-dev-tools
```

3. Build libminigui-2.0.4-linux

```
 $ cd libminigui-2.0.4-linux
 $ ./configure
 $ make
 $ sudo make install
```
4. Install MiniGUI resources

```
 $ git clone https://github.com/VincentWei/minigui-res.git
 $ cd minigui-res
 $ ./augen.sh
 $ ./configure
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
$ qvfb -width 640 -height 480
$ cd /src $ ./startpmp
```
