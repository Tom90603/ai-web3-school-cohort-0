# Agent 协助学习日志 — Week 1

## 任务：搭建 GitHub Repo + 生成学习计划

### 任务概述
使用 Hermes Agent 完成 Week 1 的三项核心交付：
1. 配置 Learning Agent（Hermes）
2. 创建 GitHub Repo 作为学习工作区
3. 生成个人 Week 1 学习计划

### Agent 做了什么

| 步骤 | 动作 | 结果 |
|------|------|------|
| 1 | 理解课程 Week 1 任务要求 | 正确识别三个交付物：Agent 配置、GitHub Repo、学习计划 |
| 2 | 检查本地环境（git 配置、gh CLI） | 发现未安装 gh CLI，无 git 配置 |
| 3 | 安装 gh CLI（尝试 apt / 预编译 / pip 三种方式） | 最终通过 pip 装，但功能不全，改用 SSH + GitHub API |
| 4 | 创建项目目录结构 | `week1/{notes,prompts,demos,logs}/` |
| 5 | 配置 git user.name / user.email | ✅ |
| 6 | 生成 SSH Key 并指导用户添加到 GitHub | ✅ |
| 7 | 生成 README.md、resources.md、learning-plan.md、agent-config.md | 4个文件 |
| 8 | git init → commit → push 到 GitHub | ✅ 已上线 `Tom90603/task` |

### 人做了什么

| 步骤 | 说明 |
|------|------|
| 1 | 提供课程 Week 1 的完整内容 |
| 2 | 提供 GitHub 用户名（Tom90603） |
| 3 | 在 GitHub 网页创建空仓库 |
| 4 | 在 GitHub Settings 添加 SSH Key |
| 5 | 指出 README 中包含个人信息，要求清理 |

### 哪些输出可靠
- Git 操作（init、add、commit、push）100% 可靠
- 文件生成和目录结构搭建可靠
- SSH Key 生成及配置指导可靠

### 哪些不可靠 / 需人工干预
- 自动创建 GitHub Repo 受限于 Token 权限，需要用户手动建空仓库
- 初始 README 包含了不应公开的个人信息，需人工审核
- 长文本生成（学习计划）偶有 API 超时，进度需要确认

### 下一步改进
- 未来类似任务先在私有环境完成敏感内容编辑，再推送到公开 repo
- 使用课程提供的模板结构更清晰地归类笔记

---

**工具：** Hermes Agent（xiaomi-mimo 模型）
**时间：** 2026-05
