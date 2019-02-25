sudo apt-get install -y git gcc g++ binutils autoconf automake libtool make cmake pkg-config libgtk2.0-dev libjpeg-dev libpng-dev libfreetype6-dev libsqlite3-dev libxml2-dev

Build GVFB
git clone https://github.com/VincentWei/gvfb.git

```
 $ cd gvfb
 $ cmake .
 $ make; sudo make install
 $ cd ..
```

Build libminigui-2.0.4-linux


Build mGallery

git clone https://github.com/FMSoftCN/mgallery.git

```
$ ./autogen.sh
$ ./configure
$ make;
```

Default all material files are stored in '/media' dirctory. Before run mgallery, you should create '/media' directory and its subdirectories: music, video, picture, recoder, ebook, cfg.

$ mkdir /media $ mkdir /media/music $ mkdir /media/video $ mkdir /media/picture $ mkdir /media/ebook $ mkdir /media/recorder $ mkdir /media/cfg

Alternately you can define RES_TOP_DIR MACRO to set custom path.

Run mGallery

$ qvfb $ cd /src $ ./startpmp
