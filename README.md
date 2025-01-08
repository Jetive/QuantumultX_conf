# Quantumult X 配置

这是完全根据自己的情况做的配置。

## DNS
不定义任何DNS，使用运营商的DNS。

## 节点

- YToo的Trojan机场
- 自建的sixth节点，这是自建的Cloudflare Worker免费无限量节点，可以无限量使用。
    - 不能用于访问Cloudflare的IP和域名
    - ChatGPT的IP和域名是Cloudflare的IP和域名，所以不能用于访问ChatGPT

## 过滤规则

- 大部分使用sixth节点
- ChatGPT使用YToo的新加坡节点
- Cloudflare的IP和域名使用YToo的新加坡节点