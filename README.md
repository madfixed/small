![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=kenzok8&show_icons=true&&theme=transparent) <div align="center"> <h1 align="center"small</h1> <img src="https://img.shields.io/github/issues/kenzok8/small?color=green"> <img src="https://img.shields.io/github/stars/kenzok8/small?color=yellow"> <img src="https://img.shields.io/github/forks/kenzok8/small?color=orange"> <img src="https://img.shields.io/github/languages/code-size/kenzok8/small?color=blueviolet"> </div> <img src="https://v2.jinrishici.com/one.svg?font-size=24&spacing=2&color=Black">

* The small warehouse occasionally adds mainstream proxy software, ssr, passwall, homeproxy, mihomo, etc.
*
#### Usage 
  ```yaml
Default ssr and passwall plugins and dependency integration package usage: upload the integration package to the tmp directory of the openwrt device, enter the command opkg install *.ipk

The default compressed package contains ssr passwall bypass passwall2 homeproxy mihomo plugins if Install ssr and dependencies separately, rm -rf {*passwall*,*bypass*,*homeproxy*,*mihomo*}
```

* If you like to keep up with the latest, you can download small-package, which is automatically updated every day* [small -package repository address](https://github.com/kenzok8/small-package)

##### Daily plugin updates and downloads:
[![GitHub release (latest by date)](https://img.shields.io/github/v/release/kenzok8/small?style=for-the-badge&label=Plugin Download)] (https://github.com/kenzok8/small/releases/latest)

+ [ssr+passwall dependency repository](https://github.com/kenzok8/small)

+ [openwrt firmware and plugin download](https:/ /op.dllkids.xyz/)

#### Use one-key command (to prevent plugin conflicts and delete duplication)
```yaml
sed -i '1i src-git kenzo https://github.com/kenzok8/openwrt-packages ' feeds.conf.default
sed -i '2i src-git small https://github.com/kenzok8/small' feeds.conf.default
./scripts/feeds update -a && rm -rf feeds/luci/applications/luci-app-mosdns
rm -rf feeds/packages/net/{alist,adguardhome,mosdns,xray*,v2ray*,v2ray*,sing*,smartdns}
rm -rf feeds/packages/utils/v2dat
rm -rf feeds/packages/lang/golang
git clone https://github.com/kenzok8/golang feeds/packages/lang/golang
./scripts/feeds install -a
make menuconfig
``` #### Pay attention to compile the new version of Sing-box and hysteria, try to use golang version 1.22 or above, you can use the following command ```yaml
rm -rf feeds/packages/lang/golang
git clone https://github.com/kenzok8 /golang feeds/packages/lang/golang
```
