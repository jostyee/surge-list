# surge rule-set sample
### 完整的配置范例见 https://github.com/jostyee/Surge/blob/master/surge3.conf
list 文件有两种获取方式，一种是本地，一种是远程，本地的 list 文件保存到 iCloud/Surge 目录下。

```
[Rule]
DOMAIN,iosapps.itunes.apple.com,DIRECT
DOMAIN-SUFFIX,store.apple.com,DIRECT
# Rulesets
RULE-SET,SYSTEM,DIRECT
RULE-SET,https://github.com/jostyee/surge-list/raw/master/apple.list,Proxy
RULE-SET,https://github.com/jostyee/surge-list/raw/master/adblock.list,REJECT
RULE-SET,https://github.com/jostyee/surge-list/raw/master/reject.list,REJECT-TINYGIF
RULE-SET,https://github.com/jostyee/surge-list/raw/master/cn.list,DIRECT
RULE-SET,https://github.com/jostyee/surge-list/raw/master/netflix.list,NetFlix
RULE-SET,https://github.com/jostyee/surge-list/raw/master/youtube.list,YouTube
RULE-SET,https://github.com/jostyee/surge-list/raw/master/blocked.list,Proxy
RULE-SET,https://github.com/jostyee/surge-list/raw/master/telegram.list,Proxy
RULE-SET,LAN,DIRECT
# GeoIP CN
GEOIP,CN,DIRECT
FINAL,Proxy,dns-failed
