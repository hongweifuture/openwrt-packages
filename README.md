### 说明

* 软件不定期同步大神库更新，两位L大库里都删除了某软件，作为搬运工，`passwall`的依赖一并找齐

* 适合一键下载到`package`目录下，用于`openwrt`编译

* 适合 [P3TERX](https://p3terx.com/archives/build-openwrt-with-github-actions.html) 的***使用 GitHub Actions 云编译 OpenWrt***，包括其他版本云编译


### 注意
- `passwall`选编译，在`openwrt`或者`lean`源码下编译`passwall`，要 [下载此依赖库](https://github.com/hongweifuture/pwdep.git)

- [或者Lienol 的 passwall新库地址](https://github.com/xiaorouji/openwrt-passwall.git)

#### openwrt 固件编译自定义主题与软件

Applications| 说明
|- |- 
luci-app-openclash       |openclash图形         
luci-app-advancedsetting |系统高级设置
luci-theme-ifit          |透明主题（适配18.06修复主机名错误）
luci-app-aliddns         |阿里云ddns
luci-app-eqos            |依IP地址限速
luci-app-gost            |隐蔽的https代理
luci-app-adguardhome     |去广告 
luci-app-smartdns        |smartdns防污染
luci-app-passwall        |Lienol大神 
luci-app-ssr-plus        |Lean大神
luci-theme-atmaterial    |主题,tmaterial 三合一（适配18.06）   
luci-theme-argon_new     |主题,二合蓝 紫主题
luci-theme-opentomcat    |主题,修复主机名错误（适配18.06）  
luci-theme-opentomato    |主题,修复主机名错误（适配18.06） 

### 教程

#### 本地编译

1、 添加下面代码到 `openwrt` 或 `lede` 源码根目录`feeds.conf.default`文件
 
```bash
 src-git weifuture https://github.com/hongweifuture/openwrt-packages
```
2、 passwall依赖
 ```bash
 src-git pwdep https://github.com/hongweifuture/pwdep.git
 ```
- lede/package$下运行 或者openwrt/package$下运行
```bash
 git clone https://github.com/hongweifuture/openwrt-packages.git
```
#### 云编译
```bash
# Add a feed source
sed -i '$a src-git hwfuture https://github.com/hongweifuture/openwrt-packages' feeds.conf.default
sed -i '$a src-git pwdep https://github.com/hongweifuture/pwdep.git' feeds.conf.default
```

 

 


