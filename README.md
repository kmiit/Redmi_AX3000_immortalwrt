ImmortalWrt For Redmi AX3000
============================

Known issue:
------------

- Same as [openwrt-redmi-ax3000](https://github.com/hzyitc/openwrt-redmi-ax3000)
- [NAT64 and NAT66 performance degradation](https://github.com/openwrt/openwrt/issues/15857)
  > Workaround: 
  > `ifconfig | grep "^[^ ]" | grep -v lo | awk '{print $1}' | while read iface; do ethtool -K $iface gro off; done`

Default login address: http://192.168.1.1 or http://immortalwrt.lan, username: __root__, password: _none_.

How to build
============
### Requirements
```bash
sudo apt update -y
sudo apt install -y ack antlr3 asciidoc autoconf automake autopoint binutils bison build-essential \
  bzip2 ccache clang cmake cpio curl device-tree-compiler ecj fastjar flex gawk gettext gcc-multilib \
  g++-multilib git gnutls-dev gperf haveged help2man intltool lib32gcc-s1 libc6-dev-i386 libelf-dev \
  libglib2.0-dev libgmp3-dev libltdl-dev libmpc-dev libmpfr-dev libncurses-dev libpython3-dev \
  libreadline-dev libssl-dev libtool libyaml-dev libz-dev lld llvm lrzsz mkisofs msmtp nano \
  ninja-build p7zip p7zip-full patch pkgconf python3 python3-pip python3-ply python3-docutils \
  python3-pyelftools qemu-utils re2c rsync scons squashfs-tools subversion swig texinfo uglifyjs \
  upx-ucl unzip vim wget xmlto xxd zlib1g-dev zstd
```

Or

```bash
sudo bash -c 'bash <(curl -s https://build-scripts.immortalwrt.org/init_build_environment.sh)'
```

### Quickstart
```bash
# Clone this repository
git clone https://github.com/kmiit/Redmi_AX3000_immortalwrt
cd Redmi_AX3000_immortalwrt

# Update and install feeds
./scripts/feeds update -a
./scripts/feeds install -a

# Configure for your device
make menuconfig

# Build
make
```

How To install
==============
> Please refer to https://github.com/hzyitc/openwrt-redmi-ax3000?tab=readme-ov-file#how-to-install


## Related Repositories
- [openwrt-redmi-ax3000](https://github.com/hzyitc/openwrt-redmi-ax3000)
- [ImmortalWrt](https://github.com/immortalwrt/immortalwrt)
- [LuCI Web Interface](https://github.com/immortalwrt/luci): Modern and modular interface to control the device via a web browser.
- [ImmortalWrt Packages](https://github.com/immortalwrt/packages): Community repository of ported packages.
- [OpenWrt Routing](https://github.com/openwrt/routing): Packages specifically focused on (mesh) routing.
- [OpenWrt Video](https://github.com/openwrt/video): Packages specifically focused on display servers and clients (Xorg and Wayland).
