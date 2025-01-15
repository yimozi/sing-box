最好用的 sing-box 一键安装脚本 & 管理脚本，自动创建 REALITY 协议；支持 TUIC，Trojan，Hysteria2 等所有常见的协议

介绍
最好用的 sing-box 脚本

Github 地址：https://github.com/233boy/sing-box

特点
快速安装
无敌好用
零学习成本
自动化 TLS
简化所有流程
兼容 sing-box 命令
强大的快捷参数
支持所有常用协议
一键添加 VLESS-REALITY (默认)
一键添加 TUIC
一键添加 Trojan
一键添加 Hysteria2
一键添加 Shadowsocks 2022
一键添加 VMess-(TCP/HTTP/QUIC)
一键添加 VMess-(WS/H2/HTTPUpgrade)-TLS
一键添加 VLESS-(WS/H2/HTTPUpgrade)-TLS
一键添加 Trojan-(WS/H2/HTTPUpgrade)-TLS
一键启用 BBR
一键更改伪装网站
一键更改 (端口/UUID/密码/域名/路径/加密方式/SNI/等…)
还有更多…

设计理念
设计理念为：高效率，超快速，极易用

脚本基于作者的自身使用需求，以 多配置同时运行 为核心设计

并且专门优化了，添加、更改、查看、删除、这四项常用功能

你只需要一条命令即可完成 添加、更改、查看、删除、等操作

例如，添加一个配置仅需不到 1 秒！瞬间完成添加！其他操作亦是如此！

脚本的参数非常高效率并且超级易用，请掌握参数的使用

请认真往下阅读脚本的参数使用，你就会发现可以如此美妙

支持协议列表
TUIC
Trojan
Hysteria2
VMess-WS
VMess-TCP
VMess-HTTP
VMess-QUIC
Shadowsocks
VMess-H2-TLS
VMess-WS-TLS
VLESS-H2-TLS
VLESS-WS-TLS
Trojan-H2-TLS
Trojan-WS-TLS
VMess-HTTPUpgrade-TLS
VLESS-HTTPUpgrade-TLS
Trojan-HTTPUpgrade-TLS
VLESS-REALITY
VLESS-HTTP2-REALITY
Socks

机场推荐
如果你只是单纯的翻，墙需求，可以购买机场的，不用自己搭建什么的，省心省力。

机场推荐： Just My Socks

Just My Socks 是搬瓦工提供的 Shadowsocks & V2Ray 服务，不怕跑路，非国人商家，无须担心 IP 被墙问题。

购买教程： Just My Socks 详细图文购买教程

搭建教程
如果是新手，请看：sing-box 一键搭建详细图文教程

安装
系统支持：Ubuntu，Debian，CentOS，推荐使用 Ubuntu 22，谨慎使用 CentOS，脚本可能无法正常运行！

执行如下命令：

bash <(wget -qO- -o- https://github.com/233boy/sing-box/raw/main/install.sh)
如果需要指定 sing-box 版本，请在安装命令后面加 -v ver 参数

如需查看安装命令帮助，在安装命令后面加 -h 即可

安装完成
当你执行了上面的安装命令，并且没有错误提示的话，那么你就能看到类似下面的图片

sing-box 脚本安装完成
脚本特意弄了一个时间显示，给反馈用来检测安装时间的…

理论上，绝大多数情况下 15 秒内会安装完成，条件允许的情况下仅需一秒即可完成安装！

超过 15 秒的你应该考虑换 VPS 了，推荐使用 搬瓦工 VPS

为方便你快速使用，脚本在安装完成后会自动创建一个 VLESS-REALITY 配置

此时你可以复制 URL 到相关软件 (例如 v2rayN) 去测试一下是否正常使用。

如果无法正常使用，请尝试使用 sing-box add ss auto auto aes-256-gcm 添加一个 SS 来再测试一下

管理面板
安装完成后，输入 sing-box 或者 sb 就能看到管理面板，如下图片所示

sing-box 脚本管理面板
提示，如果你不想执行任何功能，直接按 Enter 回车退出即可。

为方便输入，脚本自动创建 sb 快捷输入命令用来代替 sing-box （sing-box 太长了都

无法使用
无法使用一般都是两种情况，一是无法连接上端口，二是客户端内核支持有问题。

如果你的 VPS 有外部防火墙，请确保你已经开放了端口

测试端口是否能连接上：

打开：https://tcp.ping.pe/

写上你的 VPS IP 跟端口；内容为 ip:端口，示例：1.1.1.1:443，然后点击 Go；或者直接回车

如果显示 successful；证明端口能连接；如果显示 failed；那是无法连接上端口。

提醒，你可以使用 sb ip 查看 VPS IP。

关闭防火墙，执行如下命令：

systemctl stop firewalld; systemctl disable firewalld; ufw disable

关闭防火墙之后再测试一下端口是否通，如果不通，你可能还有外部防火墙没关，必须要能连接上端口才能正常使用。

如果能连接上端口，那就继续

使用 sb add ss auto auto aes-256-gcm 添加一个 SS 看看能不能正常使用，如果正常使用，证明运行没有问题。

提醒，默认安装的 sing-box 内核为最新版本

如果无法使用，可能是你客户端的内核太旧

请尝试使用不同的客户端进行测试；比如 v2rayN；v2rayNG 等

请尝试设置 VMessAEAD，某些客户端会有相关选项

某些客户端得把 额外id(alterid) 填写为 0；比如垃圾苹果那边的东西

请更新你的客户端 sing-box 内核跟服务器端版本保持一致！

快速入门
sing-box 脚本简化了很多流程，例如我们常用的是 (添加、更改、查看、删除) 配置，以下内容让你可以快速掌握使用

添加配置：

sb add -> 添加配置

sb add reality -> 添加一个 VLESS-REALITY 配置

sb add reality 443 auto dl.google.com -> 同上，自定义参数：端口使用 443， SNI 使用 dl.google.com

sb add hy -> 添加一个 Hysteria2 配置

sb add ss -> 添加一个 Shadowsocks 2022 配置

sb add tcp -> 添加一个 VMess-TCP 配置

备注，使用 sb add 添加配置的时候，仅 *TLS 相关协议配置必须提供域名，其他均可自动化处理。

如需查看更多 add 参数用法，请查看下面的 add 说明

–

更改配置：

sb change -> 更改配置

sb change reality -> 更改 REALITY 相关配置

sb change reality sni 1.1.1.1 -> 更改 REALITY 相关配置的 SNI 为 1.1.1.1, 也可以使用 sb sni reality 1.1.1.1

sb change tcp -> 更改 TCP 相关配置

sb change tcp port auto -> 更改 TCP 相关配置的端口，端口使用自动创建，也可以使用 sb port tcp auto

如需查看更多 change 参数用法，请查看下面的 change 说明

–

查看配置：

sb info -> 查看配置

sb info REALITY -> 查看 REALITY 相关配置

sb info tcp -> 查看 TCP 相关配置

–

删除配置：

sb del -> 删除配置

sb del REALITY -> 删除 REALITY 相关配置

sb del tcp -> 删除 TCP 相关配置

提醒，谨慎使用 del 参数

–

非常棒！你已经掌握最常用的功能 (添加、更改、查看、删除)

add / change / info / del ： 添加、更改、查看、删除

对于绝大多数用户来说

使用 sb add 添加配置，使用 sb change sb info sb del 来 (更改、查看、删除) 配置即可。

提醒，如果只匹配到一个配置时则自动选择该配置，否则将显示匹配到的配置列表，要求选择其中一个配置

add
add 是一个用来添加配置的参数

备注：可选参数中使用 auto 代替即是让脚本自动化处理相关参数

用法：sb add [protocol] [args... | auto]

举例：

sb add
sb add h2
sb add ws
sb add ss
sb add hy
sb add tcp
sb add tuic
sb add reality

提醒，当 可选参数 不存在时，即默认为 auto，仅 *TLS 协议配置的域名无法自动处理。

例如，sb add tcp 等于 sb add tcp auto auto auto

–

可选参数详细说明如下：

添加一个 VLESS-REALITY 配置
可选参数：端口，UUID，SNI
用法: sb add reality [port] [uuid] [sni]
举例:

sb add reality

sb add reality 443 auto dl.google.com -> 端口使用 443，SNI 使用 dl.google.com

备注，此处的 reality 可以直接写成 r，即是 sb add r 等于 sb add reality

–

添加一个 VLESS-HTTP2-REALITY 配置
可选参数：端口，UUID，SNI
用法: sb add rh2 [port] [uuid] [sni]
举例:

sb add rh2

sb add rh2 443 auto dl.google.com -> 端口使用 443，SNI 使用 dl.google.com

–

添加一个 TUIC 配置
可选参数：端口，UUID
用法: sb add tuic [port] [uuid]
举例:

sb add tuic

sb add tuic 443 -> 端口使用 443

–

添加一个 Trojan 配置
可选参数：端口，password
用法: sb add trojan [port] [password]
举例:

sb add trojan

sb add trojan 443 -> 端口使用 443

–

添加一个 Hysteria2 配置
可选参数：端口，password
用法: sb add trojan [port] [password]
举例:

sb add hy

sb add hy 443 -> 端口使用 443

备注，此处的 hy 可以换成 hy2 Hysteria2，但是明显没有必要多输入啊（

–

添加一个 Shadowsocks 配置
可选参数：端口，密码，加密方式
用法：sb add ss [port] [password] [method]
举例：

sb add ss

sb add ss auto auto 2022-blake3-aes-128-gcm -> 加密方式使用 2022-blake3-aes-128-gcm

sb add ss 233 233boy aes-128-gcm -> 端口使用 233，密码使用 233boy.com，加密方式使用 aes-128-gcm

–

添加一个 Socks 配置
可选参数：端口，密码，加密方式
用法：sb add socks [port] [username] [password]
举例：

sb add socks

sb add socks 233 233boy 233boy.com -> 端口使用 233，用户名使用 233boy，密码使用 233boy.com

–

添加一个 VMess-(WS/TCP/HTTP/QUIC) 配置
可选参数：端口，UUID，伪装类型
用法：sb add [ws | tcp | http | quic] [port] [uuid]
举例：

sb add ws -> 添加一个 VMess-WS 配置

sb add tcp -> 添加一个 VMess-TCP 配置

sb add http -> 添加一个 VMess-HTTP 配置

sb add quic -> 添加一个 VMess-QUIC 配置

sb add tcp 233 auto -> 端口使用 233，UUID 自动创建

–

添加一个 VMess-(WS/H2/HTTPUpgrade)-TLS 配置
可选参数：域名，UUID，路径
用法: sb add [ws | h2 | hu] [host] [uuid] [/path]
举例:

sb add wss -> 添加一个 VMess-WS-TLS 配置

sb add h2 -> 添加一个 VMess-H2-TLS 配置

sb add hu -> 添加一个 VMess-HTTPUpgrade-TLS 配置

sb add wss 233boy.com -> 域名使用 233boy.com

sb add h2 233boy.com auto /h2 -> 域名使用 233boy.com，路径使用 /h2

sb add hu 233boy.com auto /mypath -> 域名使用 233boy.com，路径使用 /mypath

–

添加一个 VLESS-(WS/H2/HTTPUpgrade)-TLS 配置
可选参数：域名，UUID，路径
用法: sb add [vws | vh2 | vhu] [host] [uuid] [/path]
举例:

sb add vws -> 添加一个 VLESS-WS-TLS 配置

sb add vh2 -> 添加一个 VLESS-H2-TLS 配置

sb add vhu -> 添加一个 VLESS-HTTPUpgrade-TLS 配置

sb add vws 233boy.com -> 域名使用 233boy.com

sb add vh2 233boy.com auto /h2 -> 域名使用 233boy.com，路径使用 /h2

sb add vhu 233boy.com auto /HTTPUpgrade -> 域名使用 233boy.com，路径使用 /HTTPUpgrade

–

添加一个 Trojan-(WS/H2/HTTPUpgrade)-TLS 配置
可选参数：域名，UUID，路径
用法: sb add [tws | th2 | vhu] [host] [uuid] [/path]
举例:

sb add tws -> 添加一个 Trojan-WS-TLS 配置

sb add th2 -> 添加一个 Trojan-H2-TLS 配置

sb add vhu -> 添加一个 Trojan-HTTPUpgrade-TLS 配置

sb add tws 233boy.com -> 域名使用 233boy.com

sb add th2 233boy.com auto /h2 -> 域名使用 233boy.com，路径使用 /h2

sb add vhu 233boy.com auto /HTTPUpgrade -> 域名使用 233boy.com，路径使用 /HTTPUpgrade

–

提醒，sb add [protocol] 的 protocol 也可以换完整的协议名称，名称看上面的支持协议列表

举例，sb add Hysteria2 跟 sb add hy 是一样的，但当然还是用简化的名称吧，简单好记。

举例，sb add Shadowsocks 跟 sb add ss 是一样的，但当然还是用简化的名称吧，简单好记。

再说一遍，当可选参数不存在时默认是自动化处理的 (除了 *TLS 的配置必须提供域名)，如非必要，可以省去使用可选参数的。

所以，绝大多数情况下，只要加上协议即可，举例： sb add tcp，sb add hy，sb add tuic

no-auto-tls
no-auto-tls 参数跟 add 参数用法一样，但禁止自动配置 TLS, 可用于 *TLS 相关协议

用法：sb no-auto-tls [protocol] [args... | auto]

举例：

sb no-auto-tls
sb no-auto-tls wss
sb no-auto-tls vh2 233boy.com
sb no-auto-tls vhu 233boy.com

提醒，如果你想要手动配置 TLS，请使用此选项，例如你想要用 NGINX 实现 TLS

帮助说明：sing-box 脚本 no-auto-tls 参数帮助说明

[name]
试想一虾，如果你当前有 233 个 VMess-TCP 配置的时候，如何快速选择其中一个配置呢

当你有多个配置时，你可以使用 [name] 关键词用来匹配相关配置，以便于快速执行 更改，查看，删除 等操作

推荐使用 端口 或者 域名 来匹配，这样更加容易筛选相关配置。

请往下查看会使用到 [name] 的举例

提醒，如果只匹配到一个配置时则自动选择该配置，否则将显示匹配到的配置列表，要求选择其中一个配置

change
change 是一个用来更改配置的参数

用法: sb change [name] [option] [args... | auto]

提醒：不同的配置可提供更改的相关选项是不同的

[option] 名称及选项说明参数如下：

名称	可选参数	用途	auto
full	[…]	更改多个参数	其他
id	[uuid]	更改 UUID	是
host	[domain]	更改域名	-
port	[port]	更改端口	是
path	[/path]	更改路径	是
passwd	[passowrd]	更改密码	是
key	[Private key] [Public key]	更改密钥	是
method	[method]	更改加密方式	是
sni	[domain]	更改 serverName	是
new	[…]	更改协议	其他
web	[domain]	更改伪装网站	-
备注，支持 auto 的即是可以将可选参数设置为 auto，以执行自动更改相关参数

如果 auto 为其他，可选参数请参考 add 参数用法，full 类似于 sb add 当前协议 [...]，new 类似于 sb add [...]

举例:

sb change -> 更改配置

sb change tcp -> 更改一个 tcp 相关的配置

sb change tcp port 233 -> 更改一个 TCP 配置的端口为 233

sb change tcp port auto -> 更改一个 TCP 配置的端口，并且端口自动创建

sb change tuic id auto -> 更改一个 TUIC 配置的 UUID，并且 UUID 自动创建

sb change tls host 233boy.com -> 更改一个 tls 配置的域名为 233boy.com

sb change tls web example.com -> 更改一个 tls 配置的伪装网站为 example.com

sb change reality sni 1.1.1.1 -> 更改一个 reality 配置的 SNI 为 1.1.1.1

提醒， [option] 名称也支持直接使用

用法：sb [option] [name] [...]

举例：

sb id -> 更改 UUID

sb port -> 更改 端口

sb port tcp 233 -> 更改一个 tcp 配置的端口为 233

sb id tcp -> 更改一个 tcp 配置的 UUID

sb id tcp auto -> 更改一个 tcp 配置的 UUID，并且 UUID 自动创建

sb host tls 233boy.com -> 更改一个 tls 配置的域名为 233boy.com

sb web tls example.com -> 更改一个 tls 配置的伪装网站为 example.com

sb sni reality 1.1.1.1 -> 更改一个 reality 配置的 SNI 为 1.1.1.1

更改配置的选项较多，就不一个一个举例了，绝大多数情况下使用 sb change 即可

info
info 是一个用来查看配置的参数

用法: sb info [name]

举例:

sb info -> 查看配置

sb info tcp -> 查看一个 tcp 配置

sb info tuic -> 查看一个 tuic 配置

sb info tls -> 查看一个 tls 配置

import
import 是一个用来导入 xray/v2ray 脚本配置的参数，方便统一管理

使用: sb import

仅限使用本人(233boy)的 xray/v2ray脚本创建的配置可自动导入

仅部分配置可实现自动导入，并且已导入的配置，将在原脚本上无法查看或管理

url
url 是一个生成配置的 URL 链接的参数

用法: sb url [name]

举例:

sb url -> 查看配置的 URL 链接

sb url tcp -> 查看一个 tcp 配置的 URL 链接

sb url hy -> 查看一个 Hysteria2 配置的 URL 链接

sb url tls -> 查看一个 tls 配置的 URL 链接

qr
qr 是一个用来生成配置的二维码的参数

用法: sb qr [name]

举例:

sb qr -> 查看配置的二维码

sb qr tcp -> 查看一个 tcp 配置的二维码

sb qr hy -> 查看一个 Hysteria2 配置的二维码

sb qr tls -> 查看一个 tls 配置的二维码

del
del 是一个用来删除配置的参数

用法: sb del [name]

举例:

sb del -> 删除配置

sb del tcp -> 删除一个 tcp 配置

sb del tuic -> 删除一个 tuic 配置

sb del tls -> 删除一个 tls 配置

谨慎使用此选项

ddel
ddel 是一个用来删除多个配置的参数

用法: sb ddel [name...]

举例:

sb ddel -> 删除配置

sb ddel tcp tuic -> 同时删除一个 tcp，一个 tuic 配置

提醒，此处的 [name] 只有匹配到相关配置是唯一时，才会执行删除

例如，假设你当前有两个 tcp 配置，使用 sb ddel tcp 是不会删除任何文件的

谨慎使用此选项

gen
gen 参数跟 add 参数用法一样，但是 gen 参数只返回 JSON 内容，不会创建配置，仅供测试使用

用法：sb gen [protocol] [args... | auto]

举例：

sb gen ss
sb gen tcp
sb gen hy2
sb gen tuic
sb gen reality 2333
sb gen vws 233boy.com

bbr
bbr 参数是启用 BBR 优化的

使用: sb bbr

bin
bin 参数是直接调用 sing-box 核心运行相关命令，此参数可完全兼容所有 sing-box 命令

用法：sb bin [...]

举例：sb bin help

默认兼容的命令： check | completion | format | generate | geoip | geosite | merge | rule-set | run | tools

举例：sb generate uuid

fix-config.json
fix-config.json 参数是用来修复 config.json 文件的

使用: sb fix-config.json

update
update 参数是用来更新的

用法：sb update [core | sh | caddy] [ver]

举例:

sb update -> 更新核心
sb update core -> 更新核心
sb update core v1.8.13 -> 更新核心，使用 v1.8.13 版本
sb update sh -> 更新脚本
sb update caddy -> 更新 Caddy

log
log 参数是用来查看 sing-box 运行的实时日志

使用：sb log

status
status 是查看运行状态的参数

使用：sb status

start, stop, restart
start, stop, restart 是管理 sing-box 启动，停止，重启 的参数

用法：sb [start | stop | restart] [caddy]

举例：

sb restart -> 重启 sing-box
sb restart caddy -> 重启 Caddy

reinstall
reinstall 是重装脚本的参数

使用: sb reinstall

uninstall
uninstall 是卸载脚本的参数

使用：sb uninstall

设置DNS
请看：sing-box 脚本 DNS 设置

中转
如果你需要使用 A 机器转发流量到 B 机器

那么请看：sing-box 脚本中转教程

帮助
哎呀，不想写了，其他的一些参数用法，请查看帮助

使用：sb help

目录
sing-box 脚本全部身家保存在 /etc/sing-box

脚本：/etc/sing-box/sh
核心：/etc/sing-box/bin
配置：/etc/sing-box/conf

不要为什么不符合 XXX 规则，因为我更想符合一键删除理念。

友情提醒
如果你添加了 *TLS 协议的配置，请务必设置伪装网站，使用 sb web tls 快速设置伪装网站

伪装网站
伪装网站是一个反代，指的是打开自己域名的时候显示来自伪装网站的内容

自动 TLS 说明
sing-box 脚本自动 TLS 帮助说明

备份脚本
考虑到可能会有不可描述的事情发生，你可以将 sing-box 脚本备份一下以防止万一。

Github 地址：https://github.com/233boy/sing-box

你可以 Fork 一份，如果本人一键删库跑路了，你也可以照样正常安装使用

安装命令如下：

wget https://github.com/233boy/sing-box/archive/main.tar.gz -O sing-box-main.tar.gz;tar -zxvf sing-box-main.tar.gz;cd sing-box-main;chmod +x i*;./i* -l
记得要把安装命令中的 233boy 更改成你的 Github 用户名

关注我们
Telegram 频道：https://t.me/tg2333

Telegram 群组：https://t.me/tg233boy

反馈问题
https://github.com/233boy/sing-box/issues
# 介绍

最好用的 sing-box 一键安装脚本 & 管理脚本

# 特点

- 快速安装
- 无敌好用
- 零学习成本
- 自动化 TLS
- 简化所有流程
- 兼容 sing-box 命令
- 强大的快捷参数
- 支持所有常用协议
- 一键添加 VLESS-REALITY (默认)
- 一键添加 TUIC
- 一键添加 Trojan
- 一键添加 Hysteria2
- 一键添加 Shadowsocks 2022
- 一键添加 VMess-(TCP/HTTP/QUIC)
- 一键添加 VMess-(WS/H2/HTTPUpgrade)-TLS
- 一键添加 VLESS-(WS/H2/HTTPUpgrade)-TLS
- 一键添加 Trojan-(WS/H2/HTTPUpgrade)-TLS
- 一键启用 BBR
- 一键更改伪装网站
- 一键更改 (端口/UUID/密码/域名/路径/加密方式/SNI/等...)
- 还有更多...

# 设计理念

设计理念为：**高效率，超快速，极易用**

脚本基于作者的自身使用需求，以 **多配置同时运行** 为核心设计

并且专门优化了，添加、更改、查看、删除、这四项常用功能

你只需要一条命令即可完成 添加、更改、查看、删除、等操作

例如，添加一个配置仅需不到 1 秒！瞬间完成添加！其他操作亦是如此！

脚本的参数非常高效率并且超级易用，请掌握参数的使用

# 文档

安装及使用：https://233boy.com/sing-box/sing-box-script/

# 帮助

使用：`sing-box help`

```
sing-box script v1.0 by 233boy
Usage: sing-box [options]... [args]...

基本:
   v, version                                      显示当前版本
   ip                                              返回当前主机的 IP
   pbk                                             同等于 sing-box generate reality-keypair
   get-port                                        返回一个可用的端口
   ss2022                                          返回一个可用于 Shadowsocks 2022 的密码

一般:
   a, add [protocol] [args... | auto]              添加配置
   c, change [name] [option] [args... | auto]      更改配置
   d, del [name]                                   删除配置**
   i, info [name]                                  查看配置
   qr [name]                                       二维码信息
   url [name]                                      URL 信息
   log                                             查看日志
更改:
   full [name] [...]                               更改多个参数
   id [name] [uuid | auto]                         更改 UUID
   host [name] [domain]                            更改域名
   port [name] [port | auto]                       更改端口
   path [name] [path | auto]                       更改路径
   passwd [name] [password | auto]                 更改密码
   key [name] [Private key | atuo] [Public key]    更改密钥
   method [name] [method | auto]                   更改加密方式
   sni [name] [ ip | domain]                       更改 serverName
   new [name] [...]                                更改协议
   web [name] [domain]                             更改伪装网站

进阶:
   dns [...]                                       设置 DNS
   dd, ddel [name...]                              删除多个配置**
   fix [name]                                      修复一个配置
   fix-all                                         修复全部配置
   fix-caddyfile                                   修复 Caddyfile
   fix-config.json                                 修复 config.json
   import                                          导入 sing-box/v2ray 脚本配置

管理:
   un, uninstall                                   卸载
   u, update [core | sh | caddy] [ver]             更新
   U, update.sh                                    更新脚本
   s, status                                       运行状态
   start, stop, restart [caddy]                    启动, 停止, 重启
   t, test                                         测试运行
   reinstall                                       重装脚本

测试:
   debug [name]                                    显示一些 debug 信息, 仅供参考
   gen [...]                                       同等于 add, 但只显示 JSON 内容, 不创建文件, 测试使用
   no-auto-tls [...]                               同等于 add, 但禁止自动配置 TLS, 可用于 *TLS 相关协议
其他:
   bbr                                             启用 BBR, 如果支持
   bin [...]                                       运行 sing-box 命令, 例如: sing-box bin help
   [...] [...]                                     兼容绝大多数的 sing-box 命令, 例如: sing-box generate uuid
   h, help                                         显示此帮助界面

谨慎使用 del, ddel, 此选项会直接删除配置; 无需确认
反馈问题) https://github.com/233boy/sing-box/issues
文档(doc) https://233boy.com/sing-box/sing-box-script/
```
