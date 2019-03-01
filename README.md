forgottenserver 7.4
===============

Based on a downgraded branch by [@ninjalulz](https://github.com/ninjalulz/), which according to the file 'definition.h' is **TFS 1.2**. The original [Forgotten Server](https://github.com/otland/forgottenserver/) is a free and open-source MMORPG server emulator written in C++. It is a fork of the [OpenTibia Server](https://github.com/opentibia/server) project. Custom client included (7.72 client with 7.4 dat/spr/pic).

### Getting Started 

* [Compiling](https://github.com/otland/forgottenserver/wiki/Compiling)
* [Scripting Reference](https://github.com/otland/forgottenserver/wiki/Script-Interface)

### Support

If you need help, please visit the [our OTLand forum thread](https://otland.net/threads/7-4-tfs-1-2.245320/).

### Issues

We use the [issue tracker on GitHub](https://github.com/babymannen/theforgottenserver-7.4/issues).


# Name of the Project, if there is a space in the name use either an _ or a - in its place
TFS='TFS'
# Go to the Home directory and make a Project directory
cd ~
mkdir $TFS && cd $TFS
# TFS - Server
sudo apt-get install -y git cmake build-essential liblua5.2-dev libgmp3-dev libmysqlclient-dev libboost-system-dev libboost-iostreams-dev libpugixml-dev
# Go to the Project directory
cd ~/$TFS
# Git
git clone --recursive https://github.com/otland/forgottenserver.git
# Compile
cd forgottenserver && mkdir build && cd build && cmake .. && make
cp tfs ../
sudo apt-get update
