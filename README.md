# ClashFiles

## 已对 Clash v1.8.0 做出针对性适配，同时建议更低版本的 Clash 用户及时升级，以免出现间歇性断网

#### 项目频道：https://t.me/ClashFiles_Channel 欢迎来关联群组玩，我会尽力帮助各位

1. 两个 ACL4SSR ini 为本人由 [ACL4SSR](https://github.com/ACL4SSR/ACL4SSR) 的现有 ini 配置拼凑而来，使用了ACL4SSR(_Online).ini 的ruleset 与ACL4SSR_Online_Full.ini 的国家节点分组，并自行添加了各国节点、回国节点等新节点分组。
2. GeneralClashConfig.yml 作为 Clash 配置模版由 ACL4SSR_Online_Full.ini 调用。
3. config.yaml 为自用 Clash for Windows 配置文件，由 ACL4SSR版修改而来：主要添加（修改）了 DNS 配置，修改了几个值，添加网易云解锁子进程。
4. pref.yml为自用 subconverter 的配置文件（使用方法：直接放进 subconverter.exe 所在目录即可，默认调用优先级高于pref.ini），主要应用了本项目 ACL4SSR_Full.ini 中的 ruleset 与节点分组，启用了 catch、异步获取， 并添加了网易云节点分组，添加了本地解锁（端口16375）以及几个自己收集的公共节点（已在节点名中备注来源）。
5. UnblockNeteaseMusic.yml 为纯网易云解锁配置文件，只带有网易云解锁功能。
## 个人整理 Clash 项目地址

#### 一、Clash 项目地址（只放流行的，推荐顺序自上而下）
Clash 官方已支持 SSR （不支持加密方式 chacha20），此处 ClashR 仅作备用。


1. 内核

原版：
https://github.com/Dreamacro/clash

ClashR(BROBRID)：
https://github.com/BROBRID/clash

ClashR(frainzy1477)：
https://github.com/frainzy1477/clashrdev

2. Windows 客户端

Clash for Windows：
https://github.com/Fndroid/clash_for_windows_pkg

PS:两个 Clash For Windows 汉化版，风格各异，请自行挑选
1. ~~https://github.com/HoldOnBro/LocalizeCFW~~ 停更
2. https://github.com/BoyceLig/Clash_Chinese_Patch

ClashWeb（内存占用超少）：
https://github.com/lzdnico/ClashWeb

3. Android 客户端

Clash for Android：
https://github.com/Kr328/ClashForAndroid

ClashR for Android(BROBRID)：
https://github.com/BROBRID/ClashForAndroid
通常只跟进较稳定版本

4. MacOS 客户端

ClashX：
https://github.com/yichengchen/clashX

ClashXR(Whojave)：
https://github.com/WhoJave/clashX
目前暂停更新

ClashXR(XinSSS)
https://github.com/XinSSS/clashX
非常新的一个版本，目前仍然在更新

#### 二、一些实用工具

subconverter（订阅转换后端）
https://github.com/tindy2013/subconverter

subweb（网页前端，差不多是一个前者的GUI）
https://github.com/lzdnico/subweb/tree/admin

