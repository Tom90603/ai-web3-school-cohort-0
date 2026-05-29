# 🌉 Bridge 层工作流链路图

> 产出时间：2026-05-27（重绘于 2026-05-29）| 学员：Tom90603

## Agent 链上工作流

### 阶段① Chain-aware Context（链感知上下文）

- 读取：chain id、合约地址、ABI、余额、授权、交易历史、区块数据
- 链上状态需要标明来源：区块号、交易哈希、explorer link

### 阶段② Web3 Tool Use（工具调用）

| 类型 | 说明 |
|:---|:---|
| 核心原则 | 读写分离 — Contract Read ≠ Write |
| 只读 | RPC Tool / Contract Read |
| 写链 | Contract Write / Wallet Tool |
| 执行前检查 | 权限 + 额度 + 模拟（simulation）|

### 阶段③ Agent Workflow（智能体工作流）

- **Task Graph**：目标拆解成节点
- **State Machine**：明确阶段状态
  - draft → context_loaded → plan_ready → waiting_user_confirmation → submitted → done
- **Trace**：每一步都有记录

### 阶段④ Human-in-the-loop（人工复核）

| 风险等级 | 处理方式 |
|:---|:---|
| 只读分析 | 自动执行 |
| 交易草稿 | 自动生成 |
| 小额白名单 | Session Key 自动签名 |
| 高风险交易 | 人工确认 |
| 超出范围 | 直接拒绝 |

### 阶段⑤ 签名上链

- 签名方式：用户签名 / Session Key / 多签
- 提交交易 → 等待确认
- 失败处理：判断是否已广播 → 停止或重试

### 阶段⑥ 验证结果 + 记录

- 记录：交易哈希 + explorer link
- 写入 Trace
- 回应用户 + 更新上下文
