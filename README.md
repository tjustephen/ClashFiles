# ClashFiles

## 本项目主要用于存放一些自用的 Clash 有关文件。

1. 两个 ACL4SSR ini 为本人由 [ACL4SSR](https://github.com/ACL4SSR/ACL4SSR) 的现有 ini 配置拼凑而来，使用了ACL4SSR(_online).ini 的ruleset 与ACL4SSR_Online_Full.ini 的国家节点分组，并自行添加了俄国节点、回国节点等新节点分组。

2. GeneralClashConfig.yml 作为 Clash 配置模版由 ACL4SSR_Online_Full.ini 调用。
3. config.yaml 为自用 Clash for Windows 配置文件，由 ACL4SSR版修改而来，主要添加（修改）了 DNS 配置，修改了几个值以满足日用。
4. pref.ini 为自用 subconverter 的配置文件，主要应用了本项目 ACL4SSR_Full.ini 中的 ruleset 与节点分组，启用了 catch、异步获取， 并添加了网易云节点分组，添加了本地（端口16375）以及几个自己收集的公共节点（已在节点名中备注来源）。