# Learning Agent 配置说明

## 主工具：Hermes Agent

**版本**：最新（git 安装）
**运行位置**：WSL (Ubuntu 24.04) + 阿里云 ECS（双实例）
**项目路径**：`~/my_hermes/`
**虚拟环境**：`~/my_hermes/venv/`

## 启动方式

```bash
cd ~/my_hermes
source venv/bin/activate
hermes              # 交互模式（默认 profile: main）
```

## Profile 配置

运行两个独立 Hermes 实例，分别用于不同场景。

## 模型配置

```yaml
# config.yaml 关键部分
model:
  default: xiaomi-mimo
  provider: xiaomi
```

Provider: xiaomi（小米 Mimo API）
Base URL: https://api.xiaomimimo.com/v1
环境变量: XIAOMI_API_KEY

备用模型：deepseek-chat（之前主用）

## 分身库（知识库）

- ChromaDB 位置：`~/.hermes_knowledge/`
- Collection 名：`my_knowledge`
- 设计原则：不修改旧记录，只追加新记录
- 云 ECS 同步：有副本

## 已安装 Skills

| Skill | 用途 |
|-------|------|
| cross-analysis-framework | 横纵分析法，研究任何对象 |
| bilibili-video-analysis | B站视频下载+Whisper转写+分析 |
| notion | Notion API 对接 |
| feishu-lark-gateway-debug | 飞书网关调试 |
| hermes-cloud-migration | ECS 部署指南 |
| design-knowledge-system-builder | Design KB 搭建 |

## 学习日志（首次使用）

将本课程的 Week 1 介绍、任务拆解和推荐材料交给 Hermes 后，Hermes 生成了这份学习计划（见 notes/learning-plan.md），并用 execute_code 工具完成了 GitHub repo 的目录搭建和文件生成。

**模型表现**：xiaomi-mimo 在中文理解上表现良好，但长上下文生成时偶有超时。复杂任务（如生成完整计划）建议拆分成小步骤。

## 安全说明

- Hermes 配置了 yolo 模式，但涉及签名、转账、合约写入等操作仍保持人工确认
- 私钥/助记词永远不会交给 AI Agent
- 所有链上操作先在测试网完成
