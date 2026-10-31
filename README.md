# ChatGPT 充值指南：国内怎么开通 Plus（代充、官网、App Store）

> **利益相关声明**：本仓库由 [Plus宇宙](https://www.pluscosmo.com/)（ChatGPT 自有账号人民币充值服务）维护，文中代充流程以维护方的流程为例。本仓库与 OpenAI、Apple 没有隶属、授权或合作关系；ChatGPT、Codex 是 OpenAI 的商标。官方规则都附了来源链接，**以官方页面和你账号内显示为准**。
>
> 核验日期：2026-10-31 · 姊妹篇：[Codex 充值指南](https://github.com/cc-studi0/codex-daichong)

搜「ChatGPT充值」「ChatGPT代充」的人，多数要的是给**自己的** ChatGPT 账号开通或续费会员，并弄清官网、App Store、代充哪条路适合自己。这份指南按这个需求整理，持续更新。

任何渠道都**不应**要求你提供 ChatGPT 密码、短信 / 邮箱验证码或双重验证恢复码。对方一旦要这些，马上停止。

---

## 目录

1. [先搞清楚：ChatGPT 充值，充的是什么](#1-先搞清楚chatgpt-充值充的是什么)
2. [三条实际路径对比](#2-三条实际路径对比官网--app-store礼品卡--代充)
3. [官方美元档位速查](#3-官方美元档位速查)
4. [代充流程：四步](#4-代充流程四步)
5. [想买 Plus：专节](#5-想买-plus专节)
6. [避坑清单](#6-避坑清单)
7. [靠谱平台检查清单](#7-靠谱平台检查清单)
8. [常见问题 FAQ](#8-常见问题-faq)
9. [更新日志](#9-更新日志)
10. [免责声明](#10-免责声明)

---

## 1. 先搞清楚：ChatGPT 充值，充的是什么

「ChatGPT 充值」充的是 **ChatGPT 付费订阅（Go / Plus / Pro）**，开在你自己的账号上。账号有了对应档位的订阅，才能使用该档位的用量和功能。

它**不是**：

- OpenAI **API 平台余额**：开发者按用量计费，和会员是两套账单（来源：[Managing billing for ChatGPT and the API platform](https://help.openai.com/en/articles/9039756-managing-billing-for-chatgpt-and-the-api-platform)）；
- 别人注册好的**成品号**，或多人共用的**拼车号**；
- 单独的「Codex 会员」：Codex 用量跟着 ChatGPT 方案走，Free 和 Go 也能用，只是用量和功能有限（来源：[Using Codex with your ChatGPT plan](https://help.openai.com/en/articles/11369540-using-codex-with-your-chatgpt-plan)）。

动手前先对号入座：

| 你的情况 | 实际要办的事 | 正确入口 |
| --- | --- | --- |
| 想用 ChatGPT 付费能力，账号还是 Free | 开通 Go / Plus / Pro 订阅 | 本指南主角：下文三条路径 |
| 已是 Plus / Pro，只是某段时间不够用 | 官方补充用量（credits）或评估是否升档 | 账号内「设置 → 用量」；不要再买一份同档会员来“顶量” |
| 用 API Key 调用模型或做自动化 | API 平台余额 | [OpenAI 开发者平台](https://platform.openai.com/)，与 ChatGPT 会员完全两套账单 |
| 其实只想把 Codex 用起来 | 仍是给 ChatGPT 开会员（或买 credits） | 另见 [Codex 充值指南](https://github.com/cc-studi0/codex-daichong) |

后两种情况买会员解决不了：会员不含 API 余额；ChatGPT 内的 credits 也不是 API credits（来源：[Using Credits for Flexible Usage](https://help.openai.com/en/articles/12642688-using-credits-for-flexible-usage-in-chatgpt-personal-plans)）。

---

## 2. 三条实际路径对比（官网 / App Store·礼品卡 / 代充）

国内常见、能实际走通的就是这三条。共享账号、拼车、成品号单独列出，不推荐正式使用。

| 路径 | 能否微信 / 支付宝 | 账号归属 | 主要风险 | 适合谁 |
| --- | --- | --- | --- | --- |
| 官网直接订阅（chatgpt.com） | 否，通常需要国际卡 + 受支持地区 | 自己的账号 | 拒付、账单地址不一致；在不支持地区使用可能影响账号 | 有稳定海外卡、且使用环境符合官方支持地区的人 |
| App Store 内购 / 礼品卡 | 视 Apple ID 区服与余额来源而定 | 自己的账号 | 中国大陆／香港区常搜不到官方 App；外区 ID 与礼品卡来源有风险；取消和退款都找 Apple | 已有能付款的外区 Apple ID 的 iPhone 用户 |
| 代充（第三方为自有账号开通） | 是，多数平台支持人民币 | 自己的账号（正规交付的话） | 渠道质量参差不齐：跑路、售后找不到人、要密码 | 没有海外支付方式、想用人民币一次办完的人 |

**共享账号 / 拼车 / 成品号（不推荐）**

- 账号往往**不归你**，原主或卖家可能改密码、收回，或者共用你的对话。
- OpenAI 使用条款写明不得共享账号凭据或让他人使用账号；Pro 说明页也写明共享凭据、转售访问权限属于被禁止的行为，可能因此被限制访问（来源：[Terms of Use](https://openai.com/policies/terms-of-use)、[About ChatGPT Pro tiers](https://help.openai.com/en/articles/9793128-about-chatgpt-pro-tiers)）。
- 隐私无法保证：对话、上传的文件，同车的人都可能看到。
- 如果只是临时体验，优先用 Free 或 Go，比拼车干净。

> 表里的“风险”针对的是付款和账号归属这一环。会员的功能与用量由账号的官方档位决定，跟你从哪条路径付款无关。

**路径怎么粗选**

- 有外币卡且使用环境符合官方要求 → 走官网最短。
- 有可用的外区 Apple ID → 走 App 内购。
- 两样都没有、只有微信 / 支付宝 → 代充；付款前用第 7 节的检查清单筛选渠道。

**官网路径的常见卡点**

1. 登录 [chatgpt.com](https://chatgpt.com/)，点头像 → Upgrade plan，选档后填卡和账单地址。
2. 国内发卡常被拒付。官方[支持地区列表](https://help.openai.com/en/articles/7947663-chatgpt-supported-countries)不含中国大陆与中国香港，官方写明在列表以外的地区访问可能导致账号被封禁或停用。
3. 付款成功后，以 **设置 → 账户** 里的方案名为准。

**App Store / 礼品卡路径的常见卡点**

1. 需要能下载官方 ChatGPT App 的区服 Apple ID；部分区服的商店页长期不可用。
2. 外区余额常靠礼品卡充值：只从可信渠道获取，价格明显低于面值的不要碰。
3. 订阅由 Apple 管理：取消在 iPhone **设置 → 你的名字 → 订阅**；退款也找 Apple。卸载 App 不会自动取消订阅（来源：[Canceling your ChatGPT subscription](https://help.openai.com/en/articles/7232927-canceling-your-chatgpt-subscription)）。

---

## 3. 官方美元档位速查

个人付费方案的官方月费（美元）：

| 档位 | 官方月费 | 说明（摘要） |
| --- | --- | --- |
| Go | $8（美国标价；部分地区为本地化定价） | 轻量档；不含 Codex Cloud |
| Plus | $20 | 多数个人用户的日常主力 |
| Pro 100 | $100 | Pro 入门档 |
| Pro 200 | $200 | 用量多于 Pro 100；2026-10 官方已撤销此前公告的用量下调 |
| Pro 500 | $500 | 三档中用量最高；唯一包含 Ultrafast 的个人方案 |

来源：

- [What is ChatGPT Plus?](https://help.openai.com/en/articles/6950777-what-is-chatgpt-plus)
- [About ChatGPT Pro tiers](https://help.openai.com/en/articles/9793128-about-chatgpt-pro-tiers)
- [Introducing ChatGPT Go](https://openai.com/index/introducing-chatgpt-go/)（$8 为美国标价，官方注明部分市场本地化定价）、[What is ChatGPT Go?](https://help.openai.com/en/articles/11989085-what-is-chatgpt-go)
- Codex 相关权益对照：[Codex Pricing](https://learn.chatgpt.com/docs/pricing)

几个容易忽略的官方口径：

- Go、Plus、Pro **只能按月付**，官方不支持年付或预付多个月。
- **会员不包含 API 额度**。
- 在哪里买就在哪里退订：官网订阅在 ChatGPT 设置里取消，App Store 订阅在 Apple 那边取消。卸载 App 不等于取消订阅。
- 各档位之间的用量差距，官方没有给出相对 Plus 的固定倍数；商家标注的“5X / 10X / 25X”之类说法**不是官方口径**。
- 人民币实际花费因渠道而异（汇率、手续费、礼品卡溢价、代充平台标价都不同），**一律以你付款当次的结算页为准**。

---

## 4. 代充流程：四步

代充的核心是：你用人民币付款，由平台为**你自己的** ChatGPT 账号开通或续费对应方案。正规交付一般只需要临时会话凭据（Session），不需要密码。

以本仓库维护方的流程为例（逐步截图见 [充值教程](https://www.pluscosmo.com/guide)；其他平台大同小异）：

### 步骤 1：选档

先想清楚要 Go、Plus 还是 Pro 哪一档，再到[套餐页](https://www.pluscosmo.com/shop)核对周期和当日价格。

账号里如果**已经有有效订阅**，先确认归属（官网 / Apple / Google Play）和到期日，问清平台怎么衔接，避免两份订阅同时计费。

### 步骤 2：提交 Session

登录自己的 ChatGPT，按结算页说明复制临时 Session，粘贴回订单页。

- 全程不需要密码、验证码、恢复码。
- Session 在一段时间内可能等同于登录权限：只填在平台自己的 HTTPS 订单页，不要发到群聊、私聊，也不要截图外传。
- 开通完成后，可以在 ChatGPT 设置里退出所有设备，让这份 Session 尽快失效。

### 步骤 3：付款

用微信或支付宝在**平台生成的订单里**付款，保留订单号。不要按“客服私聊”的要求转账到个人账户。

### 步骤 4：验收

处理完成后，用**同一个**账号登录官方 ChatGPT，到 **设置 → 账户** 核对：

1. 方案名称（Go / Plus / Pro 及 Pro 档位）是否正确；
2. 有效期 / 下次扣费日是否合理。

**只认账号内显示，不凭“能聊天了”或订单状态单独判断。** 如果仍显示 Free，先确认是不是登错了号，尤其是用 Apple「隐藏邮件地址」登录的情况（来源：[What is ChatGPT Plus?](https://help.openai.com/en/articles/6950777-what-is-chatgpt-plus) 的 “Charged but still on Free plan” 一节）。处理时效以订单页和平台说明为准，不要只听口头的“秒到”。

---

## 5. 想买 Plus：专节

搜「ChatGPT Plus 购买」的人，多数合理的默认选择是：**日常主力用 Plus**。

什么时候优先选 Plus：

- 每天写作、办公、学习、轻度编程，Free / Go 明显不够用；
- 需要进阶模型和 Codex、深度研究等能力，但还没到整天顶格用的程度。

什么时候再考虑 Pro：

- Plus 的用量**反复**卡住真正要交付的工作（不是偶尔失败一次）；
- 长时间重度使用 Codex 或深度研究，用 credits 补量后仍然不够（Plus 触限后可以直接买 credits，不必先升档）。

Codex 用量和速度模式的细节，见本仓 [docs/codex.md](docs/codex.md) 和姊妹篇 [Codex 充值指南](https://github.com/cc-studi0/codex-daichong)。

---

## 6. 避坑清单

- 要密码、短信 / 邮箱验证码、2FA 恢复码的“代充”→ 立刻停，换渠道。
- 只收 Session，但没有订单号、进度页，全靠私聊口头承诺 → 谨慎。
- 要求转账到个人账户、绕过站内订单的“内部渠道”→ 不要付。
- 会员还在有效期内，又重复购买**同档**订阅 → 可能两处同时计费。
- 为了 API 余额去买会员 → 两套账单，互不抵扣。
- 把成品号 / 拼车当成“ChatGPT 充值”→ 账号往往不归你，也不是给自有账号开通。
- 价格明显离谱，却承诺“必不封号”“官方一样”→ 当作营销话术，不要当成保证。
- 不要去找“黑卡 / 白卡 / 某卡商出卡”这类操作；礼品卡失败时，换正规代充或换支付方式就行。

---

## 7. 靠谱平台检查清单

付款前逐项核对。有多项做不到，就换一家（不必追求满分，优先看凭据和订单这两项）。

**凭据安全**

1. 不要 ChatGPT 密码、邮箱密码、验证码、恢复码。
2. 提交凭据的入口是平台自己的 HTTPS 页面，而不是发到个人微信或来历不明的第三方表单。
3. 写明凭据用完后怎么处理，以及你自己怎样让 Session 失效。

**价格与交付**

4. 价格明码标出，并写清周期（例如 1 个月 / 按官方账期）。
5. 写清交付物：是给你**自己的账号**开会员，而不是给你一个新号。
6. 写清已有订阅时怎么衔接，不默认“会自动叠加”。
7. 不承诺官方都做不到的事（例如“锁定永久旧额度”“绝不封号”）。

**订单、售后与验收**

8. 有订单号和状态页，付款后能查进度。
9. 质保 / 退款规则写清楚，并写明哪些情况**不包括**（例如账号被封）。
10. 只在平台订单内付款；平台也要求你登录官方账号核对方案和到期日。

能开发票、页面好看、价格低，都不能单独证明靠谱。更有用的信号是：要的凭据最少、规则写在页面上、出了问题能凭订单号找到人。

---

## 8. 常见问题 FAQ

**Q1：ChatGPT 充值和 ChatGPT 代充有什么区别？**
在中文搜索里基本是同一个需求：用人民币（或借助第三方）给账号开通或续费会员。真正要区分的是**交付方式**——开在你自己的账号上，还是卖你一个别人的号。前者才是本指南说的充值 / 代充。

**Q2：Plus 购买和充值是一回事吗？**
对个人用户来说通常是：买 Plus 就是给账号开通 Plus 订阅，区别只在付款路径（官网、App Store、代充）。

**Q3：代充会不会封号？**
没有人能替官方保证不封号。更稳妥的做法是：只选订单可查、不碰密码的渠道；自己遵守使用条款和支持地区规则。凡是承诺“零风险 / 必不封号 / 官方认可”的，反而要警惕。

**Q4：会员里含 API 余额吗？**
不含。会员和 API 是两套独立计费，需要 API 就去开发者平台充值（来源：[What is ChatGPT Plus?](https://help.openai.com/en/articles/6950777-what-is-chatgpt-plus)）。

**Q5：和「Codex 充值」是什么关系？**
Codex 的用量跟着 ChatGPT 方案走，所以很多“Codex 充值”需求，本质上还是给 ChatGPT 开 Plus / Pro，或者买 credits。详见 [Codex 充值指南（GitHub）](https://github.com/cc-studi0/codex-daichong)。

**Q6：付完钱怎么验收才算到账？**
登录同一个账号，看官方账户页的**方案名称和有效期**。能发消息、能看到某个模型，都不能单独证明已到账。App 端显示异常的话，可以试试「恢复购买」（只适用于应用商店订阅）。

**Q7：已经是 Plus，还能再买一个月叠加吗？**
不要默认能叠加。官方不支持预付多个月。先查清当前订阅是从哪里付的、什么时候到期、有没有自动续费，再问清平台怎么衔接。

**Q8：官网能不能直接用微信 / 支付宝？**
官网的可用支付方式因国家而异（来源：[What is ChatGPT Go?](https://help.openai.com/en/articles/11989085-what-is-chatgpt-go) 中关于 Multi-currency billing 的说明）。中国大陆不在官方支持地区内，国内用户一般无法直接用微信 / 支付宝在官网订阅；没有海外支付方式时，常见的选择是外区 App Store，或人民币代充。

---

## 9. 更新日志

| 日期 | 变更 |
| --- | --- |
| 2026-10-31 | 顶部加入利益相关声明（由 Plus宇宙 维护），删除“独立整理”的表述；正文里维护方的站点链接收敛到 3 处（声明、套餐页、充值教程），价格类、选型类外链改为官方来源；档位表补充 Go 本地化定价说明、Pro 200 用量下调已撤销、Pro 500 独享 Ultrafast；新增“商家倍数标注不是官方口径”；共享账号一节改引使用条款与 Pro 说明页原文；新增 MIT 许可证；同步更新 docs/codex.md。 |
| 2026-10-27 | 按「ChatGPT充值 / 代充」主词重构：澄清充什么 → 三条路径 → 官方美元速查 → 代充四步 → Plus 专节 → 避坑 → 检查清单 → FAQ；互链 Codex 仓。 |
| 2026-10-20 | 首版（方式对比体裁）：官方美元档位、路径说明、平台清单与 FAQ。 |

发现过时信息，欢迎提 Issue 并附上官方链接。

---

## 10. 免责声明

- 本文只整理公开信息和常见操作路径，不构成购买建议。价格、方案、可购地区与规则可能随时变化，**以 OpenAI、Apple 官方页面和你的账号内显示为准**。
- 第三方充值平台（包括本仓库维护方）不是 OpenAI 的官方渠道，OpenAI 不为任何第三方背书。使用前请自行评估风险，并遵守 [OpenAI 使用条款](https://openai.com/policies/terms-of-use)和所在地法律法规。
- 下单金额以各平台结算页当日显示为准。
- 本仓库采用 [MIT](LICENSE) 许可，转载请注明出处。
