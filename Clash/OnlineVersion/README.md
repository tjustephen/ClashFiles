# 一点说明

## 基于本地规则碎片的外部配置

没有添加 clash_rule_base 字段。

在本地配置条件下，通过config.yml文件本身来定义显然更加通用。

## 基于云端规则碎片的外部配置

提供两种不同dns enhanced-mode模式的配置文件。

其中redir_host适合有应用将clash单纯作为dns的情况下使用。

建议使用clash http/socks/mixin port的用户使用redir-host

使用clash Tap/TUN/透明代理模式的用户使用fake-ip模式

## 如何同时切换TUN/Tap模式与clash dns enhanced-mode 字段值（仅CFW）

配置文件内设定为redir-host

并在 Mixin 中将两者的配置写在一起

例：
``` yaml
mixin:
  dns:
    enhanced-mode: fake-ip
  tun:
   enable: true
   stack: system 
   dns-hijack:
     - 198.18.0.2:53 
   auto-route: true
   auto-detect-interface: true
```
