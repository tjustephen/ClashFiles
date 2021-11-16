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
