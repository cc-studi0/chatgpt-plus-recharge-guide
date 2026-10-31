# Codex 订阅、充值与价格详解（2026-10）

> 核验日期：2026-10-31。数据来自 OpenAI 的 [Codex 定价页](https://learn.chatgpt.com/docs/pricing)、[Pro 方案说明](https://help.openai.com/en/articles/9793128-about-chatgpt-pro-tiers)、[Codex 与 ChatGPT 方案说明](https://help.openai.com/en/articles/11369540-using-codex-with-your-chatgpt-plan) 和 [Credits 说明](https://help.openai.com/en/articles/12642688-using-credits-for-flexible-usage-in-chatgpt-personal-plans)。规则变化很快，以官方页面和你账号里的用量页面为准。
>
> 利益相关：本仓库由 Plus宇宙 维护，与 OpenAI 无隶属关系。
>
> ← 返回 [ChatGPT 充值 / 代充指南](../README.md)

## 1. Codex 到底怎么收费

Codex 没有单独的会员，计费有两条路：

| 路径 | 怎么登录 | 怎么计费 | 适合 |
|---|---|---|---|
| ChatGPT 账号登录 | 用 ChatGPT 账号登录 Codex（App、CLI、IDE 插件、网页） | 用方案自带的用量；Plus / Pro 用完可以买 credits | 个人日常开发 |
| API Key 登录 | 在 CLI / SDK / IDE 插件里填 API Key | 按 API 价格逐 token 计费 | CI 和自动化；**不支持**云端功能（GitHub 代码审查、Slack 等） |

另外，官方定价页写明 **ChatGPT Work 和 Codex 共用同一份额度**；ChatGPT for Excel 等智能体功能开始计费后，也会共用这份额度（目前包括 Plus 和 Pro 上的 ChatGPT for Excel）。

## 2. 各方案的 Codex 权益

| 方案 | 月费（美元） | Codex 权益 |
|---|---|---|
| Free | $0 | 桌面 App 中以标准速度使用 GPT-6 Luna（逐步开放）；不含 Codex Cloud |
| Go | $8（美国标价；部分地区为本地化定价） | 同上，定位“轻量编程任务”；不含 Codex Cloud |
| Plus | $20 | 网页、CLI、IDE 插件、iOS；自动代码审查、Slack 集成；GPT-6.1 Sol 和 GPT-6 Luna；可以买 credits |
| Pro 100 / 200 / 500 | $100 / $200 / $500 | Plus 的全部权益加更高用量；Ultrafast 只在 Pro 500 上有 |

关于 Pro 三档的用量差距：

- 官方只说明“Pro 200 的用量多于 Pro 100，Pro 500 是三档中最高的”，**没有给出相对 Plus 的固定倍数**。第三方商品页上的“5X / 10X / 25X”之类命名是商家标注，不是官方倍数。
- 2026-10 官方更新：此前公告的 Pro 200 用量下调**已撤销**，Pro 200 重新开放新订阅；Pro 100 和 Pro 500 的 Work / Codex 用量翻倍；Plus 不变（来源：[About ChatGPT Pro tiers](https://help.openai.com/en/articles/9793128-about-chatgpt-pro-tiers)）。
- Go、Plus、Pro 都只能按月订阅，不支持年付或预付多个月。

> 2026 年 10 月 14 日起，用 ChatGPT 账号登录的 Codex 不再提供 GPT-5.5；用 API Key 登录的不受影响（来源：Codex 定价页）。

## 3. Plus 大概能用多少

官方给的是**每 5 小时本地消息数的估算**（Plus 和标准 Business 相同），不是固定上限：

| 模型 | Plus 每 5 小时本地消息（估算） |
|---|---|
| GPT-6 Astra | 5–45 |
| GPT-6.1 Sol | 15–160 |
| GPT-6.1 Terra | 35–285 |
| GPT-6 Sol | 15–150 |
| GPT-6 Luna | 350–3,000 |

- 本地消息和云端任务共用额度，云端任务通常更费；此外**可能还有每周上限**。
- 官方写明 **Pro 目前没有 5 小时限制**（以后可能变）。
- 区间这么大，是因为消耗取决于模型、上下文大小、推理量、工具调用和缓存命中，而不是你发了几句话。

## 4. 速度模式会多耗额度

| 速度模式 | 消耗会员自带用量 | 消耗已购 credits |
|---|---|---|
| Fast | 2.5 倍 | 2 倍 |
| GPT-6 Astra Ultrafast | 8 倍 | 6 倍 |
| GPT-6.1 Sol Ultrafast | 8 倍 | 6 倍 |

倍率都是相对同一模型的标准模式。Ultrafast 只在 Pro 500 上有，开启后额度消耗非常快，只在确实赶时间时用。另外，带图像生成的轮次平均会多消耗 3–5 倍额度。

## 5. Credits：额度用完后的“充值”

- **怎么扣**：先用完方案自带的用量，再扣 credits。
- **在哪里买**：ChatGPT 的 **设置 → 用量**，或者 Codex App 的 **Usage & Billing**；Plus 和 Pro 在 Codex 里触限时也会弹出购买入口。Free 和 Go 目前只有少数用户可以购买。
- **价格**：可购买的数量、价格和支付方式因账号、地区和方案而异，**以你账号内购买页显示为准**（本文不再列出具体价格）。
- **能用在哪**：Codex、ChatGPT Work、ChatGPT for Word / Excel / PowerPoint 等符合条件的功能，**不是所有功能都能用**。
- **有效期与退款**：自购买起 12 个月有效，过期作废；原则上不退款，不能转让或转售。
- **余额可能变成负数**：任务开始时余额是正的，跑的过程中被并发任务用完，余额就会变负；之后再买的 credits 会先补上负数部分。
- **和钱包不是一回事**：credits 余额和 ChatGPT 钱包（礼品卡兑换的美元余额）是分开的，兑换礼品卡不会直接变成 credits。也不是 API credits。
- 官方定价页按每百万 token 列出各模型消耗多少 credits，例如 GPT-6.1 Sol 输入 50、输出 250 credits；官方举例说 GPT-5.6 Sol 的一个典型任务大约用 2–15 credits。

## 6. 怎么选：按使用强度

| 你的情况 | 建议 |
|---|---|
| 想先试试 Codex 能不能用起来 | Free 或 Go，在桌面 App 里跑几个小任务 |
| 每周有几次集中写代码 | Plus（官方原话：“每周几次专注的编程会话”） |
| Plus 偶尔触限，一周一两次 | 留在 Plus，触限时买少量 credits |
| Plus 天天触限、影响交付 | Pro 100；先看一个账期的用量页面，再决定要不要 200 / 500 |
| 要在 CI 或脚本里跑 | 用 API Key，单独算 API 预算，别拿会员额度来估 |

## 7. 让额度更耐用（官方建议整理）

1. 指令写准确，去掉不必要的上下文。
2. 只给相关文件，能缩小目录范围就缩小。
3. 讲清楚输出要什么格式、多长，把必做和可选分开。
4. 控制 `AGENTS.md` 的体积，大项目可以按目录嵌套放。
5. 不用的 MCP 服务器先关掉，每多一个都会增加上下文。
6. 在 CLI 里随时用 `/status` 看剩余额度；每一两周看一次用量页面，了解自己的节奏。

## 8. 用人民币开通 Codex 能用的会员

没有海外卡的话，开通方式和普通 ChatGPT 会员完全一样：官网、外区 App Store，或者第三方充值平台。对比和风险见 [主文档第 2 节](../README.md#2-三条实际路径对比官网--app-store礼品卡--代充)。要注意：

- 第三方平台卖的是 **ChatGPT 会员**，不是“Codex 账号”。开在哪个账号上，Codex 就要用哪个账号登录。
- 如果你缺的是 **API 余额**，开会员解决不了。
- 已经开了 Plus、只是暂时额度不够，先考虑 credits，不必急着升 Pro。
- 第三方的人民币价格会变动，请以各平台结算页的实时价格为准。本仓库维护方的套餐与实时价格见 [Plus宇宙 套餐页](https://www.pluscosmo.com/shop)。

## 更新日志

| 日期 | 变更 |
|---|---|
| 2026-10-31 | 删除具体人民币价格和 App Store credits 价格，改为“以实时页面为准”；维护方链接收敛到 1 处；修复返回主文档的失效锚点；Go 标注美国标价与本地化定价；补充 Pro 200 用量下调已撤销、官方无固定倍数的说明；Plus 估算表补 GPT-6.1 Terra；补充 credits 有效期、退款与转让规则；加入利益相关声明。 |
| 2026-10-20 | 首版：各方案 Codex 权益、Plus 每 5 小时估算、速度模式倍率、credits 规则与 App Store 价格、GPT-5.5 下线说明。 |
