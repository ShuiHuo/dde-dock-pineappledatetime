## dde-dock datetime plugin (modified version)

English | [简体中文](README.md)

*Please notice that this is **NOT** an official project*

### Screenshot

![Screenshot of pineappledatetime](https://github.com/ShuiHuo/dde-dock-pineappledatetime/raw/media/带日期的时间截图.png)

### Info

Simple quick hack to make it display year/month/day on it's `Dock::Efficient` mode. Also some really little simple tweak to make it compilable without fetching the full dde-dock repo.

Current codebase is fork from [dde-dock#39c1a6b](https://github.com/linuxdeepin/dde-dock/commit/39c1a6b609c65026a505bd6b74a451bff26ee456). You can checkout the commit history and do a `diff` to see what I did changed.

### Usage

We assume you already enabled a `deb-src` source in your `/etc/apt/sources.list` thus you can use `apt build-dep <pkg-name>` to install build depts. Then you need do `apt build-dep dde-dock` first, and install `dde-dock-dev` package by doing `apt install dde-dock-dev`. Of course you can also install the build depts manually if you like.

To compile and run:

``` bash
# you should clone it first:
git clone https://github.com/ShuiHuo/dde-dock-pineappledatetime.git && cd dde-dock-pineappledatetime/
# create a folder for building it:
mkdir build
cd build/
# then build it:
cmake ../
make
# then you got `libpineappledatetime.so`
# this will copy this into `/usr/lib/dde-dock/plugins/`
sudo make install
# finally, restart `dde-dock` (kill it and dde will restart it automatically)
killall dde-dock
```

> Notice: You can put your plugin inside `~/.local/lib/dde-dock/plugins/` instead of `/usr/lib/dde-dock/plugins/` after dde-dock version `4.10.4` (version `>4.10.4`).

Then done!

### License

GPLv3 (as required, same as original license)
