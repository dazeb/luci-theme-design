# luci-theme-neobird
## 针对移动端优化的Openwrt主题

六年前用OP，随手把luci-theme-material改成了自己喜欢的Advancedtomato样式
因为用了很短时间便没再用OP了，主题也没再管。
后来便有了lede固件默认使用material主题的修改版做主题，包括今天的luci-theme-netgear和luci-theme-argon还是我的思路，不过都不是我喜欢的样子。
还有一些luci-theme-atmaterial之类的都是当时我的样式表改的，还存在于某些固件中。

前几天又用上了OP做旁路，顺手又改了一把，然后随便找了个LOGO(netgear arlo)，起了个名字，编译了一下。

## 主要特点（仅针对iOS设备，未测试安卓）：
* 针对移动端优化，特别适合手机端做为webapp使用；
* 修改很多细节，尽量视觉统一（但由于luci插件开发不规范，页面结构有些杂乱，难免有些小问题无法修正）；
* 极简易用设计，移动端去除繁杂信息，隐藏了提示信息（可能并不适合OP新手，请手机横屏查看提示文本）；
* 简洁的登录界面，底部导航栏，类App的沉浸式体验；
* 适配深色模式，适配系统自动切换；
* 全(tou)新(lai)的APP桌面图标；
* Retina图片适配。

## 体验Webapp方法：
* 在移动端(iOS/iPadOS)浏览器打开管理界面，添加到主屏幕即可。
* 想要实现完全的沉浸式（无浏览器导航、无地址栏等）体验，需要使用SSL证书，请自行申请域名、证书、安装并启用。
* 如果不使用SSL证书，基于安全原因，iOS/iPadOS 在打开新的页面后，将会显示浏览器顶部菜单栏。

## 关于其它
* 你可以改来自己用，也可以继续优化共享，但如果想改进后共享给他人，请再三确认自己的审美能力，以确保不是丑化我的成果
* 因为用了arlo的logo，请勿用于商业用途
* 我可能会在某个时间改掉logo
* luci插件众多，不规范的插件可能会存在显示问题，不做保证

## 预览
![iOS](https://github.com/thinktip/luci-theme-neobird/blob/main/preview/IMG_5916.JPEG)
![iOS](https://github.com/thinktip/luci-theme-neobird/blob/main/preview/IMG_5915.JPEG)
![iOS](https://github.com/thinktip/luci-theme-neobird/blob/main/preview/IMG_5909.JPEG)
![iPadOS](https://github.com/thinktip/luci-theme-neobird/blob/main/preview/IMG_0103.JPEG)
## 自行编译：

```
cd lede/package/lean  
rm -rf luci-theme-neobird  
git clone https://github.com/thinktip/luci-theme-neobird.git  
cd ~/lede/
make menuconfig #choose LUCI->Theme->Luci-theme-neobird  
make -j1 V=s
```
