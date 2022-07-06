## 如何同时切换TUN/Tap模式与clash dns enhanced-mode 字段值（仅CFW）

配置文件内设定为redir-host

并在 Mixin 中将两者的配置写在一起

例：
``` yaml
mixin: # object
  dns:
    enable: true # 是否启用dns false
    ipv6: false
    listen: 0.0.0.0:53
    enhanced-mode: fake-ip # 模式：redir-host或fake-ip
    fake-ip-range: 198.18.0.1/16
    fake-ip-filter: # fake ip 白名单列表，如果你不知道这个参数的作用，请勿修改
      - '*.lan'
      - localhost.ptlogin2.qq.com
    default-nameserver:
      - 223.5.5.5 # 阿里DNS
      - 119.29.29.29 # 腾讯DNS
      #- 117.50.10.10 # ONE DNS纯净版 直接返回其真实的响应结果
    nameserver:
      #- 180.76.76.76 # 百度DNS
      #- 119.29.29.29 # 腾讯DNS
      #- 117.50.11.11 # ONE DNS拦截版 恶意网站拦截、广告过滤
      #- 114.114.114.114 # 114DNS
      - https://dns.alidns.com/dns-query # 阿里 DoH DNS
      - https://doh.pub/dns-query #腾讯DNSPod DOH
      - https://dns.rubyfish.cn/dns-query # 红鱼 DoH DNS
      #- https://dns.nextdns.io/dns-query # NextDNS DOH
      #- https://doh.360.cn/dns-query # 360 DoH DNS
    fallback:
      #- 8.8.8.8 # Google DNS
      #- 1.1.1.1 # Cloudflare DNS
      #- https://dns.alidns.com/dns-query # 阿里 DoH DNS
      #- https://dns.rubyfish.cn/dns-query # 红鱼 DoH DNS
      - https://dns.nextdns.io/dns-query # NextDNS DOH
      - https://cloudflare-dns.com/dns-query # Cloudflare DoH DNS
      - https://doh.opendns.com/dns-query # OpenDNS DoH
      - https://doh.dns.sb/dns-query # DNS.sb DoH
      #- https://dns.google/dns-query # Google DoH DNS
    fallback-filter:
      geoip: true # 默认
      ipcidr: # 在这个网段内的 IP 地址会被考虑为被污染的 IP
        - 240.0.0.0/4

  tun:
   enable: true
   stack: system 
   dns-hijack:
     - 198.18.0.2:53 
   auto-route: true
   auto-detect-interface: true
```
