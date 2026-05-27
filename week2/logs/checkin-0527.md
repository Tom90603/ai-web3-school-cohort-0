📅 共学营打卡 | 2026.05.27 | Week 2

**今日内容：** 🌉 Bridge 层全景理解
- 链感知上下文（Chain-aware Context）—— 链上状态如何进入 Agent 上下文
- Web3 工具调用（Web3 Tool Use）—— RPC/合约/钱包工具的设计边界
- 智能体工作流（Agent Workflow）—— 任务图 + 状态机 + Human-in-the-loop

**🎯 完成：**
- ✅ 读完 3 篇 Bridge 手册页面
- ✅ 产出链路图：Agent 接收任务 → 读取链上状态 → 工具调用 → 人工复核 → 签名上链 → 验证结果
- ✅ 写了 3 个 PM 视角的关键思考

**💡 关键收获：**
- 链上状态不能靠模型记忆，必须从工具和索引层读取并带来源证据（区块号、交易哈希）
- 读写分离是 Web3 Agent 工具设计的核心原则——Contract Read 和 Contract Write 必须是不同工具、不同权限
- Human-in-the-loop 的分层策略很实用：自动执行 / Session Key / 人工确认 / 直接拒绝
- 作为 PM，最关注的是"怎么让用户确认交易时一眼看懂自己签了什么"

**⏱ 用时：** ~30min

**产出文件：**
- `experiments/bridge-workflow.md` — 完整链路图（流程图 + PM 思考）
