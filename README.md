# Quantumult X 配置

这是一个针对个人使用场景优化的 Quantumult X 配置文件，主要特点是注重节省流量和提高访问速度。

## 资源

### 1. 官网

- 真官网（虽然什么都没有）
  - https://quantumult.app/x/
- GitHub
  - https://github.com/crossutility/Quantumult-X
- 假官网（虽然假，但提供了一些教程，还挺有用）
  - https://quantumultx.org/

### 2. 新手教程

- https://github.com/kjfx/QuantumultX

对于入门有用，会了之后就没什么收获了。

### 3. 资源解析器

机场网站无 Quantumult X 订阅链接的，SS/SSR订阅链接可以使用，如果是V2Ray和Trojan订阅链接不能直接导入 Quantumult X ，

需要添加一个`资源解析器`，使`用资源解析器`后，可以将 Quantumult X 不识别的`节点或订阅链接`轻松的导入。

``` 资源解析器
resource_parser_url=https://raw.githubusercontent.com/KOP-XIAO/QuantumultX/master/Scripts/resource-parser.js
```

``` 资源解析器备用链接
resource_parser_url=https://fastly.jsdelivr.net/gh/KOP-XIAO/QuantumultX@master/Scripts/resource-parser.js
```

### 4. 两位大神的配置规则

- https://raw.githubusercontent.com/Orz-3/QuantumultX/master/Orz-3.conf
- https://raw.githubusercontent.com/w37fhy/QuantumultX/master/QuantumultX_diy.conf

主要是参考用，不会写的时候去看看人家怎么写的。第二个参考价值更大。

### 5. 规则List

- https://github.com/blackmatrix7/ios_rule_script

提供了分流规则用的各种List，非常全，分门别类，配置的时候直接去取。

### 6. 图标

- https://github.com/Orz-3

提供了配置文件中用到的策略图标和节点图标，好看有趣。

## 基本信息

- 配置更新时间：2025-01-10 23:00
- 配置作者：玛卡巴卡

## 策略组设置

### 主要策略组
- **节点选择**：作为总开关，可手动选择不同的策略
- **自动选择**：每10分钟自动测速选择最快节点（从0.2倍流量的节点中选择）
- **sixth**：自动选择 CF_ 开头节点中最快的
- **区域节点**：香港、美国、新加坡、日本（均为自动选择最快节点）
- **漏网之鱼**：处理未匹配规则的流量

## 订阅节点

1. **sixth节点**
   - 基于 Cloudflare Worker 的免费无限量节点
   - 更新周期：24小时
   - 订阅地址：https://sixth.visaservices.sbs/nijiucaiba/pty

2. **YTOO Trojan**
   - 商业机场节点
   - 更新周期：24小时

## 分流规则

### 直连规则
- 局域网和中国IP
- 国内云服务
- 国内网站和域名
- 微信
- CloudflareCN
- Apple 全系服务
- Microsoft 基础服务（除Copilot）
- OneDrive（为节省流量）

### 代理规则
- **走 sixth 线路**（节省流量）
  - YouTube
  - Telegram

- **走新加坡节点**
  - Cloudflare
  - GitHub
  - Copilot
  - Bing

### 特殊域名处理
直连：
- qq.com
- tencent.com
- antgroup.com
- byteimg.com
- bytedance.com
- alibaba.com
- alicdn.com
- bilibili.com 相关
- 其他国内常用域名

## DNS 设置
- 保留系统 DNS 设置
- 包含多个特殊域名的 DNS 解析规则
- 设置了 DNS 防污染机制

## 注意事项
1. 配置中包含了防 DNS 污染的设置
2. 自动策略组每10分钟进行一次测速
3. 所有 Apple 服务走直连以节省流量
4. OneDrive 虽走直连但网页版可能无法访问
5. Copilot 必须走代理才能正常使用

## 配置特点
1. 注重流量节省：大文件下载和高频访问服务优先直连
2. 智能分流：境外服务自动选择最快节点
3. 稳定性优先：关键服务指定可靠节点
4. 自动化程度高：多数情况下无需手动切换节点