ImmortalWrt For Redmi AX3000
============================

Known issue:
------------

- Same as [openwrt-redmi-ax3000](https://github.com/hzyitc/openwrt-redmi-ax3000)

Default login address: http://192.168.1.1 or http://immortalwrt.lan, username: __root__, password: _none_.

How to build (Ubuntu 24)
============
### Requirements
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
# Or check CI scrip for basic config.

# Build
make -j$(nproc)
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
