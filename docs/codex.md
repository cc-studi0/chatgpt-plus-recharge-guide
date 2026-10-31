# Codex 计费细节：我自己核对过的那几张表（2026-10）

> 这份文档是主指南的技术补充，只讲机制细节：额度怎么算、credits 怎么扣、速度模式吃多少。主流程与避坑见 [README](../README.md)。
>
> 核验日期：2026-10-31。来源：[Codex 定价页](https://learn.chatgpt.com/docs/pricing)、[Pro 方案说明](https://help.openai.com/en/articles/9793128-about-chatgpt-pro-tiers)、[Codex 与 ChatGPT 方案说明](https://help.openai.com/en/articles/11369540-using-codex-with-your-chatgpt-plan)、[Credits 说明](https://help.openai.com/en/articles/12642688-using-credits-for-flexible-usage-in-chatgpt-personal-plans)。规则变化快，以官方页面和你账号里的用量页为准。

## 一、Codex 的两条计费路径

Codex 没有单独会员，只有两种登录方式决定钱从哪来：

| 路径 | 怎么登录 | 怎么计费 | 我什么时候用它 |
|---|---|---|---|
| ChatGPT 账号登录 | App、CLI、IDE 插件、网页 | 用方案自带用量；Plus / Pro 用完可买 credits | 日常开发，占我 95% 的时间 |
| API Key 登录 | CLI、SDK、IDE 插件里填 Key | 按 API 价格逐 token 计费 | CI 和自动化；**不支持**云端功能（GitHub 代码审查、Slack 等） |

官方定价页写明 **ChatGPT Work 和 Codex 共用同一份额度**；ChatGPT for Excel 等智能体功能开始计费后也会共用（目前包括 Plus 和 Pro 上的 ChatGPT for Excel）。我第一次遇到「白天写完文档，晚上 Codex 就吃紧」，原因就在这。

## 二、各方案的 Codex 权益（官方口径）

| 方案 | 月费（美元） | Codex 权益 |
|---|---|---|
| Free | $0 | 桌面 App 中以标准速度使用 GPT-6 Luna（逐步开放）；不含 Codex Cloud |
| Go | $8（美国标价；部分地区为本地化定价） | 同上，定位「轻量编程任务」；不含 Codex Cloud |
| Plus | $20 | 网页、CLI、IDE 插件、iOS；自动代码审查、Slack 集成；GPT-6.1 Sol 和 GPT-6 Luna；可买 credits |
| Pro 100 / 200 / 500 | $100 / $200 / $500 | Plus 的全部权益加更高用量；Ultrafast 只在 Pro 500 上有 |

关于 Pro 三档的用量差距，官方只说「Pro 200 多于 Pro 100，Pro 500 三档最高」，**没有给相对 Plus 的固定倍数**；商品页上的「5X / 10X / 25X」是商家标注，不是官方口径。

2026-10 官方更新：此前公告的 Pro 200 用量下调**已撤销**，Pro 200 重新开放新订阅；Pro 100 和 Pro 500 的 Work / Codex 用量翻倍；Plus 不变（来源：[About ChatGPT Pro tiers](https://help.openai.com/en/articles/9793128-about-chatgpt-pro-tiers)）。另外，Go、Plus、Pro 都只能按月订阅，不支持年付或预付多个月。

> 2026 年 10 月 14 日起，用 ChatGPT 账号登录的 Codex 不再提供 GPT-5.5；用 API Key 登录不受影响（来源：Codex 定价页）。

## 三、Plus 每 5 小时能用多少（官方估算区间）

| 模型 | Plus 每 5 小时本地消息（估算） |
|---|---|
| GPT-6 Astra | 5–45 |
| GPT-6.1 Sol | 15–160 |
| GPT-6.1 Terra | 35–285 |
| GPT-6 Sol | 15–150 |
| GPT-6 Luna | 350–3,000 |

读这张表要注意三点：

- 这是**估算区间**，不是固定条数。区间跨度大，是因为消耗取决于模型、上下文大小、推理量、工具调用和缓存命中。
- 本地消息和云端任务共用额度，云端通常更费；另外**可能还有每周上限**。
- 官方写明 **Pro 目前没有 5 小时限制**（以后可能变）。

我的实测结论：同一个任务，把整个仓库换成两个文件，消耗能差三倍以上。**任务边界的清晰度，比换档位更影响你能跑多少活。**

## 四、速度模式到底多贵

| 速度模式 | 消耗会员自带用量 | 消耗已购 credits |
|---|---|---|
| Fast | 2.5 倍 | 2 倍 |
| GPT-6 Astra Ultrafast | 8 倍 | 6 倍 |
| GPT-6.1 Sol Ultrafast | 8 倍 | 6 倍 |

倍率都是相对同一模型的标准模式。Ultrafast 只在 Pro 500 上，开起来额度掉得肉眼可见，只在真赶时间时用。另外，带图像生成的轮次平均多消耗 3–5 倍额度。

## 五、credits：额度不够时的补量机制

- **怎么扣**：先用完方案自带用量，再扣 credits。
- **在哪里买**：ChatGPT **设置 → 用量**，或 Codex App 的 **Usage & Billing**；Plus / Pro 在 Codex 里触限时也会弹入口。Free 和 Go 目前只有少数用户能买。
- **价格**：数量和价格因账号、地区、方案而异，**以你账号内购买页显示为准**，本文不列具体价。
- **能用在哪**：Codex、ChatGPT Work、ChatGPT for Word / Excel / PowerPoint 等符合条件的功能，**不是所有功能都能用**。
- **有效期与退款**：购买起 12 个月有效，过期作废；原则上不退款，不可转让或转售。
- **余额可能变负**：任务开始时余额为正，跑到一半被并发任务吃穿，就会变负；之后买的 credits 先补负值。
- **和钱包不是一回事**：credits 余额与 ChatGPT 钱包（礼品卡兑换的美元余额）分开，兑换礼品卡不会变成 credits，也不是 API credits。
- 官方按每百万 token 列出各模型消耗多少 credits（例如 GPT-6.1 Sol 输入 50、输出 250 credits），并举例说一个典型任务约用 2–15 credits。

## 六、按使用强度选档（我的判断方式）

| 你的情况 | 建议 |
|---|---|
| 想先试试 Codex 能不能用起来 | Free 或 Go，在桌面 App 里跑几个小任务 |
| 每周有几次集中写代码 | Plus（官方原话：「每周几次专注的编程会话」） |
| Plus 偶尔触限，一周一两次 | 留在 Plus，触限时买少量 credits |
| Plus 天天触限、影响交付 | Pro 100；先看一个完整账期的用量页，再决定要不要 200 / 500 |
| 要在 CI 或脚本里跑 | 用 API Key，单独算 API 预算，别拿会员额度来估 |

## 七、让额度更耐用的七条（官方建议 + 我的补充）

1. 指令写准确，去掉不必要的上下文。
2. 只给相关文件，能缩小目录范围就缩小。
3. 讲清输出格式和多长，把必做与可做分开。
4. 控制 `AGENTS.md` 体积，大项目按目录嵌套放。
5. 不用的 MCP 服务器先关掉，每个都会占上下文。
6. CLI 里随时用 `/status` 看剩余额度；每一两周看一次用量页，了解自己的节奏。
7. 我补充一条：**同一层窗口连续两次被撞，就先改任务边界，别急着付钱**。这条帮我省下的钱比任何优惠都多。

## 八、用人民币开通能跑 Codex 的会员

没有海外卡时，开通方式和普通 ChatGPT 会员完全一样：官网、外区 App Store，或第三方充值平台。三条路径的对比与风险见 [主文档第三节](../README.md#三三条路径我都走过一遍)。要注意：

- 第三方平台卖的是 **ChatGPT 会员**，不是「Codex 账号」。开在哪个账号上，Codex 就要用哪个账号登录。
- 缺的是 **API 余额**时，开会员解决不了。
- 已开 Plus、只是暂时不够用，先考虑 credits，不必急着升 Pro。
- 人民币价格会变，以各平台结算页的实时价格为准。

## 更新日志

| 日期 | 变更 |
|---|---|
| 2026-10-31（第二版） | 改为第一人称技术补充体裁；新增两条计费路径的「我什么时候用」、Plus 表读法要点、credits 负数余额与钱包区分、我补充的第 7 条节流建议；移除平台推广链接与维护方表述。 |
| 2026-10-31 | 删除具体人民币价格与 App Store credits 价格；修复返回主文档的锚点；Go 标注美国标价与本地化定价；补充 Pro 200 下调已撤销、官方无固定倍数的说明；Plus 估算表补 GPT-6.1 Terra；补充 credits 有效期、退款与转让规则。 |
| 2026-10-20 | 首版：各方案 Codex 权益、Plus 每 5 小时估算、速度倍率、credits 规则。 |
