# windows vps推荐：Vultr 的 Windows 授权费怎么算？$300 赠金能抵几个月？2GB 内存够不够用？（附全套餐价格表）

Vultr 的 Windows 方案起步是 1 vCPU / 2GB 内存 / 55GB SSD，基础月费 $10，Windows 授权费 $16，合计 **$26/月**。这个总价要先记住，因为 Vultr 的授权费按 vCPU 另收，选到 4 vCPU / 8GB 时月费会变成 **$104**。$300 赠金对应优惠码 `FLY300VULTR`，官方写明新用户专享、只适用于指定产品、不能与其它优惠叠加；第三方整理称有效期 30 天，官方页面没写天数，注册后以账单页为准。

选 Windows VPS 先看三件事：Windows 授权是否另收费、内存有没有到 2GB、机房离实际用户多远。下面把 Vultr 的八档 Windows 方案、授权费年账、$300 赠金的限制，以及按场景选档一次讲清。

> 只想快速决定：挂一个远程桌面、外贸 ERP 或单开浏览器，1 vCPU / 2GB 就够，月费 $26；要跑 Chrome 多开、Selenium 或 IIS + SQL Server Express，直接看 2 vCPU / 4GB，月费 $52；5–10 人共享 RDP 从 4 vCPU / 8GB 起，月费 $104，并先确认远程桌面授权。
>
> 👉 [查看 Vultr Windows 套餐与当前授权费](https://www.vultr.com/servers/windows?ref=9738262-9J)

## Vultr 的 Windows VPS 多少钱：先把授权费算进总价

Vultr 官方 Windows 页面把价格拆成两列：Base Price 是计算资源月费，License Price 是 Windows 授权费。月合计要把两列相加，不是只看 $10 那一列。

| 方案（vCPU / 内存） | 存储 / 流量 | 基础月费 | Windows 授权费 | 月合计 | 购买 |
| --- | --- | --- | --- | --- | --- |
| 1 vCPU / 2GB | 55GB SSD / 2TB | $10 | $16 | **$26** | [开通 1 vCPU/2GB](https://www.vultr.com/servers/windows?ref=9738262-9J) |
| 2 vCPU / 2GB | 65GB SSD / 3TB | $15 | $32 | **$47** | [开通 2 vCPU/2GB](https://www.vultr.com/servers/windows?ref=9738262-9J) |
| 2 vCPU / 4GB | 80GB SSD / 3TB | $20 | $32 | **$52** | [开通 2 vCPU/4GB](https://www.vultr.com/servers/windows?ref=9738262-9J) |
| 4 vCPU / 8GB | 160GB SSD / 4TB | $40 | $64 | **$104** | [开通 4 vCPU/8GB](https://www.vultr.com/servers/windows?ref=9738262-9J) |
| 6 vCPU / 16GB | 320GB SSD / 5TB | $80 | $96 | **$176** | [开通 6 vCPU/16GB](https://www.vultr.com/servers/windows?ref=9738262-9J) |
| 8 vCPU / 32GB | 640GB SSD / 6TB | $160 | $128 | **$288** | [开通 8 vCPU/32GB](https://www.vultr.com/servers/windows?ref=9738262-9J) |
| 16 vCPU / 64GB | 1280GB SSD / 10TB | $320 | $256 | **$576** | [开通 16 vCPU/64GB](https://www.vultr.com/servers/windows?ref=9738262-9J) |
| 24 vCPU / 96GB | 1600GB SSD / 15TB | $640 | $384 | **$1,024** | [开通 24 vCPU/96GB](https://www.vultr.com/servers/windows?ref=9738262-9J) |

月合计按官方页面 Base Price 与 License Price 两项相加；计费按小时，月封顶 672 小时。表中只含计算资源和 Windows 授权，快照、额外 IP 等附加服务以结账页为准。

Vultr 官方 Windows 页面支持 Windows Server 2016、2019、2022、2025，包含 Standard、Datacenter 以及 Core、GUI 版本。许可证在部署 Windows 系统时自动包含，已有的 Windows Server 许可证不能转移到 Vultr。这一点对想自带授权的人很关键，Vultr 不接受 BYOL。

## Windows 授权费一年到底多花多少

官方表格里的授权费基本按 vCPU 线性增加，约 **$16/vCPU/月**。1 vCPU 是 $16/月，2 vCPU 是 $32/月，4 vCPU 是 $64/月，8 vCPU 是 $128/月。

| 配置 | 授权费/月 | 授权费/年 | 授权费占月合计 |
| --- | ---: | ---: | ---: |
| 1 vCPU / 2GB | $16 | $192 | 62% |
| 2 vCPU / 2GB | $32 | $384 | 68% |
| 2 vCPU / 4GB | $32 | $384 | 62% |
| 4 vCPU / 8GB | $64 | $768 | 62% |
| 8 vCPU / 32GB | $128 | $1,536 | 44% |

1–4 vCPU 档，授权费占月费约六成到近七成。你付的 $104 里，$64 是 Windows 授权，$40 才是计算资源。选 4 vCPU 的时候，多出来的核不只是加 CPU 钱，授权费也跟着翻倍。

这也是 Vultr 和 Windows 不加价商家之间最大的价差来源。Evoxt 的 VM-1 是 1核2GB / 20GB / 1TB，标价 $5.99/月，并称 Windows 零附加费；同样 1核2GB，Vultr 是 $26/月。两者配置和流量不同，不能只看单价，但 $16/月的授权费是差价里最明确的一块。Vultr 给的是 55GB SSD、2TB 流量和按小时计费，Evoxt 给的是更低月付和 Windows 不加价，选哪个取决于你更在意长期月费还是计费灵活性。

如果你只是短期验证一个 Windows 环境，按小时开一台 1 vCPU / 2GB，跑完就销毁，比直接月付更可控。👉 [查看 $300 赠金适用条件](https://www.vultr.com/coupons?ref=9738262-9J)

## $300 赠金怎么用，哪些情况用不上

Vultr 官方优惠页列出四个新用户优惠：`FLY300VULTR` 给 $300，`250VULTRFLY` 给 $250，`FLYTWOHUNDRED` 给 $200，`VULTRMATCH` 是首次充值 1:1 匹配，最高 $100。四条都写 New customers only，不能与其它优惠叠加，促销额度只适用于指定产品。

第三方汇总把 $300 的有效期写成 30 天，官方优惠页没有写天数。这个差异很关键：如果只有 30 天，$300 适合一个月内集中测试高配方案，不适合当成一年的折扣慢慢用。注册后在 Billing 页面确认额度、有效期和适用产品，不要默认它会自动到账。

另一个容易误解的点：赠金不是现金余额，不能提现，也不能假设它能抵 Windows 授权费。官方只写 select products only，Windows 实例和授权费是否在范围内，要以账户里显示的适用产品为准，拿不准就开工单问。

按总月费估算，$300 约等于 11.5 个月的 1 vCPU / 2GB（$26/月），或者 2.9 个月的 4 vCPU / 8GB（$104/月）。如果赠金不能用于 Windows 授权，实际可抵扣的金额会更少。先确认适用范围，再决定开哪一档。

## 按场景选档：多数人不需要超过 4 vCPU

**只挂一个远程桌面、外贸 ERP、单开浏览器**
1 vCPU / 2GB，$26/月。每天用几小时、跑一个 ERP 客户端、开几个网页，这档够用。Windows Server 本身会占掉一部分内存，Chrome 开到十几个标签就会吃紧，别把它当多任务机器。

**Chrome 多开、Selenium 多线程、轻量自动化**
2 vCPU / 4GB，$52/月。这是大多数小项目更稳的起点。2GB 能连上 RDP，但多开 Chrome 或同时跑几个脚本，内存很快见底；4GB 给的是余量，不是性能浪费。

**IIS + SQL Server Express、2–3 人同时在线**
2 vCPU / 4GB 起步，$52/月。SQL Server Express 有内存上限，4GB 能跑，但网站和数据库同时活跃时，4 vCPU / 8GB 的 $104/月会更稳。先上 2 vCPU / 4GB，不够再升，比一开始买 8 vCPU 更划算。

**5–10 人共享 RDP、多个自动化任务**
4 vCPU / 8GB，$104/月。多人同时登录会同时吃 CPU 和内存，Windows 的远程桌面服务还涉及 RDS 授权，Vultr 的 Windows 授权只覆盖服务器系统本身，多人共享前先确认这部分是否包含。配置够不等于授权够。

**6 vCPU / 16GB 以上**
$176/月起。多个 SQL Server 实例、高并发、重负载才需要。个人挂机、外贸单开、小团队远程办公，基本用不到这一档。Windows 授权费会跟着 vCPU 涨，买高了每个月都在多付。

## 横向看价格：Vultr 在 Windows VPS 里贵在哪

同样标“Windows VPS”，不同商家的 Windows 费用口径差别很大。下面只列已核验的配置和价格，方便判断 Vultr 的位置。

| 品牌/方案 | 配置 | Windows 费用 | 月费 | 备注 |
| --- | --- | --- | --- | --- |
| Evoxt VM-1 | 1核 / 2GB / 20GB / 1TB | 标称零附加费 | $5.99 | 月付低价，适合长期挂机 |
| 华纳云 香港 | 2核 / 4GB / 50GB SSD / 5Mbps 不限流量 | 含 Windows 镜像 | ¥196 | CN2 GIA，商家自述不限流量 |
| Contabo | 4核 / 8GB / 50GB SSD / 32TB | 按 Windows 方案标价 | $14.28 + $6.99 安装费 | 新加坡 +$3/月，美国部分机房加价 |
| Hostwinds | 1核 / 1GB / 30GB / 1TB | 按 Windows 方案标价 | $10.99–$12.74 | 两份第三方价格差约 16% |
| LightNode | 1核 / 2GB / 50GB SSD / 1TB | 按 Windows 方案标价 | $7.7 | 按小时计费 |
| eUKhost | 2核 / 2GB / 35GB | 另加 €7/月 | €18.65 + €7 | 仅英国伦敦 |

竞品价格来自第三方页面，时间从 2025-07 到 2026-07 不等。Hostwinds 两个来源差价明显，只给区间；Contabo 除月费外有一次性安装费和地区加价，首月支出会高于标价。这里只做信息对比，具体价格以各商家官网为准。

Vultr 的 1 vCPU / 2GB 是 $26/月，比 Evoxt、LightNode 的入门 Windows 方案贵不少，差价主要来自 $16/月的授权费。Vultr 的优势在按小时计费、月封顶 672 小时，短时测试可以按小时跑，不用直接买一个月；长期 7×24 挂机，月费就会明显高于 Windows 不加价的商家。要不要为这个灵活性付差价，取决于你是短期测试还是长期跑。

## RDP 连不上或卡顿，先排查这几步

Windows VPS 买完最常见的两个问题：连不上、连上后卡。

连不上先看地址和端口。Windows 自带“远程桌面连接”，搜索 `mstsc` 打开，计算机一栏填 IP；如果服务商给的端口不是默认 3389，就填 `IP:端口`，例如 `123.456.789.0:1234`。用户名通常是 `Administrator`，首次连接会弹证书警告，接受即可。Mac 没有内置 RDP 客户端，用微软官方的 Microsoft Remote Desktop。

如果 RDP 默认没开，先用控制台的 VNC 进系统：右键“此电脑” → 属性 → 远程设置 → 勾选“允许远程连接到此计算机”，再到防火墙确认 3389 端口入站规则是开放的。设置完再用 mstsc 连。

卡顿先降画质。在远程桌面连接的“显示”选项卡降低颜色深度，在“体验”选项卡关掉壁纸和视觉特效，带宽占用会明显下降。机房距离是硬伤，国内用户连欧美节点，调参数只能缓解，换到东京、首尔、新加坡等亚太节点更有效，具体哪些机房支持 Windows 以部署页可选列表为准。

## 下单前确认清单

1. **把 Windows 授权费加进总价。** Vultr 1 vCPU 是 $10 + $16，不是 $10；4 vCPU 是 $40 + $64，不是 $40。
2. **计费按小时、月封顶 672 小时。** 停止实例仍然计费，销毁才停止。短时测试跑完就销毁，别只点停止。
3. **$300 赠金先确认适用产品。** 官方写的是新用户专享、指定产品、不能叠加；Windows 实例和授权费是否在范围内，以账单页为准。
4. **2GB 是 Vultr Windows 方案的最低内存。** 官方表没有把 1GB 档列进 Windows 方案；Chrome 多开、IIS + SQL Server Express 直接看 4GB。
5. **机房选离用户近的。** 国内用户先试东京、首尔、新加坡等亚太节点，延迟比参数调优更管用。
6. **多人共享先确认远程桌面授权。** 配置够不代表授权够，5–10 人共享 RDP 前先问清楚 RDS 部分。

只挂一个 RDP 或外贸 ERP，1 vCPU / 2GB 的 $26/月就够；Chrome 多开、Selenium、IIS + SQL Server Express，2 vCPU / 4GB 的 $52/月更稳；5–10 人共享从 4 vCPU / 8GB 的 $104/月起，并先确认 RDS 授权。再往上，多数个人用户用不上。

下单前最后确认两件事：$300 赠金是否适用于你选的 Windows 实例，以及你是按月跑还是按小时跑。短时测试用按小时，跑完销毁；长期挂机再考虑月付封顶。

👉 [按你的场景开通 Vultr Windows VPS](https://www.vultr.com/servers/windows?ref=9738262-9J)
