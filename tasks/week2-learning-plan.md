# Week 2 个人学习计划

> 学员：Tom90603 | 工具：Hermes Agent | 方向：产品研究（非技术路线）
> 
> Week 2 主题：AI × Web3 交叉研究与方向选择

---

## 总览：5 天计划

| 天数 | 任务 | 产出 |
|------|------|------|
| Day 1 (Mon) | 🌉 理解 Bridge 层全景：Agent 如何与链上世界交互 | 笔记 |
| Day 2 (Tue) | 🔐 Agent 钱包与权限：权限模型、Session Key、安全边界 | 笔记 + 概念草图 |
| Day 3 (Wed) | 💰 机器支付与结算：Agent 自主支付、小额结算场景 | 笔记 |
| Day 4 (Thu) | 🆔 Agent 身份与信任：身份证明、声誉系统、可验证性 | 笔记 + 对比表 |
| Day 5 (Fri) | 🧭 方向选择：阅读前沿探索赛道，锁定 Hackathon 方向 | 赛道笔记 + 方向决策记录 |

---

## Day 1 — Bridge 层全景理解

### 目标
理解 AI Agent 如何与链上世界交互——不要只记住名词，要画出交互链路。

### Checklist
- [ ] 读 Handbook → [Bridge: Chain-aware Context](https://aiweb3.school/zh/handbook/bridge/chain-aware-context/)
- [ ] 读 Handbook → [Bridge: Web3 Tool Use](https://aiweb3.school/zh/handbook/bridge/web3-tool-use/)
- [ ] 读 Handbook → [Bridge: Agent Workflow](https://aiweb3.school/zh/handbook/bridge/agent-workflow/)
- [ ] 画一条完整链路图：**Agent 接收任务 → 读取链上状态 → 调用工具 → 人工复核 → 签名上链 → 验证结果**

### 笔记要点
- Chain-aware Context 解决了什么问题？（链上状态如何进入 Agent 上下文）
- Web3 Tool Use 里 Agent 能调用哪些工具？（RPC、钱包、合约）
- Agent Workflow 中哪些步骤需要 human-in-the-loop？

---

## Day 2 — Agent 钱包与权限

### 目标
理解 Agent 在链上的身份是什么——钱包不只是"存币"，而是权限入口。

### Checklist
- [ ] 读 Handbook → [Bridge: Agent Wallet](https://aiweb3.school/zh/handbook/bridge/agent-wallet/)
- [ ] 读 Handbook → [Wallet & Permission 赛道](https://aiweb3.school/zh/handbook/tracks/wallet-permission/)
- [ ] [可选] 读 Handbook → [Web3: Account Abstraction](https://aiweb3.school/zh/handbook/web3/account-abstraction/)
- [ ] 画一张权限模型对比表：EOA vs Smart Account vs Session Key

### 从 PM 视角问自己
- **Agent 能拿什么权限？**（转账额度、调用特定合约、操作白名单）
- **如何限制和撤销权限？**（时间限制、金额上限、多签确认）
- **这个权限模型对用户来说是否可理解？**（UX 角度）

---

## Day 3 — 机器支付与结算

### 目标
理解 Agent 之间的经济关系——机器如何自主完成支付。

### Checklist
- [ ] 读 Handbook → [Bridge: Machine Payment](https://aiweb3.school/zh/handbook/bridge/machine-payment/)
- [ ] 读 Handbook → [Bridge: Settlement & Escrow](https://aiweb3.school/zh/handbook/bridge/settlement-and-escrow/)
- [ ] 读 Handbook → [Agentic Commerce 赛道](https://aiweb3.school/zh/handbook/tracks/agentic-commerce/)

### 关键问题（PM 视角）
- 机器支付是真需求还是叙事？（用户关心的是 Agent 的服务质量，还是 Agent 怎么付钱？）
- 小额支付的痛点在哪里？（Gas 费用可能超过支付金额本身）
- Escrow（托管）在 Agent 场景中如何设计？争议如何仲裁？

---

## Day 4 — Agent 身份与信任

### 目标
理解 Agent 在链上如何被识别、授权和追踪。

### Checklist
- [ ] 读 Handbook → [Bridge: Agent Identity](https://aiweb3.school/zh/handbook/bridge/agent-identity/)
- [ ] 读 Handbook → [Bridge: Agent Trust & Reputation](https://aiweb3.school/zh/handbook/bridge/agent-trust-and-reputation/)
- [ ] 读 Handbook → [Bridge: Verifiable AI](https://aiweb3.school/zh/handbook/bridge/verifiable-ai/)
- [ ] 读 Handbook → [Verifiable Agent 赛道](https://aiweb3.school/zh/handbook/tracks/dev-tooling/)

### 产出：对比表
| 维度 | 传统互联网 | 区块链方案 | PM 评价 |
|------|-----------|-----------|---------|
| 身份标识 | 邮箱/手机号 | 地址/DID | |
| 授权方式 | OAuth/密码 | 私钥签名/Session Key | |
| 信任机制 | 平台背书 | 链上声誉/经济激励 | |
| 可验证性 | 日志/审计 | 链上记录/零知识证明 | |

---

## Day 5 — 方向选择 & Hackathon 方向锁定

### 目标
综合 Week1 + Week2 所学，选定一个方向做 Hackathon。

### Checklist
- [ ] 回顾所有前沿探索赛道：
  - [Agentic Commerce](https://aiweb3.school/zh/handbook/tracks/agentic-commerce/)
  - [Wallet / Permission](https://aiweb3.school/zh/handbook/tracks/wallet-permission/)
  - [AI Security](https://aiweb3.school/zh/handbook/tracks/ai-security/)
  - [Governance](https://aiweb3.school/zh/handbook/tracks/governance/)
  - [Dev Tooling](https://aiweb3.school/zh/handbook/tracks/dev-tooling/)
- [ ] 锁定 1-2 个方向，写 100 字说明"为什么选这个"
- [ ] 在 `experiments/` 下创建方向决策记录 `hackathon-direction.md`

### 选方向的原则（对 PM 来说）
1. **你能讲清楚** —— 如果不能用一句话说明白你这个方向想做什么，说明还没想透
2. **有产品切口** —— 不一定要做底层技术，可以做工具、界面、流程设计
3. **Week3 可落地** —— 选一个在 2 周内能做出最小 Demo 的方向

---

## Portfolio 视角

Week2 的材料可以直接放进作品集的"AI 时代设计工作流"故事线中：

> **素材**：Agent 钱包权限模型图 / Agentic Commerce 流程设计 / AI × Web3 Bridge 链路图
> 
> **叙事角度**：作为 PM/设计师，我关注的是 AI Agent 从"回答问题"到"执行链上操作"时，交互范式和安全边界发生了哪些变化——权限设计、支付流程、身份信任，这些都是产品层面绕不开的问题。

---

## 打卡模板（每日用）

```markdown
📅 共学营打卡 | 2026.05.26 | Week 2 - Day [Day序号]

**今日主题：** [填写]
**🎯 做了什么：**
- 
**💡 关键收获：**
- 
**❓ 疑问：**
- 
**⏱ 用时：** ~1.5h
```

---

*生成时间：2026-05-26 | 工具：Hermes Agent + 人工整理*
*本计划基于 Handbook + WCB 课程结构制定*
