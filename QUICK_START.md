# 快速开始指南 / Quick Start Guide

## 是的，你可以设置背后的模型！/ Yes, you can configure the model!

### 🚀 三步开始 / Three Steps to Start

#### 步骤 1 / Step 1: 选择配置方式 / Choose Configuration Method

有两种方式：
There are two methods:

- **方式 A**: 编辑 `model-config.json` (推荐用于程序化配置)
- **Method A**: Edit `model-config.json` (recommended for programmatic config)

- **方式 B**: 使用 `.env` 文件 (推荐用于开发环境)
- **Method B**: Use `.env` file (recommended for development)

#### 步骤 2 / Step 2: 配置你的模型 / Configure Your Model

**使用 model-config.json:**
```json
{
  "model": {
    "provider": "openai",     // 改成你想要的提供商 / Change to your provider
    "name": "gpt-4",          // 改成你想要的模型 / Change to your model
    "api_key": "${OPENAI_API_KEY}",
    "parameters": {
      "temperature": 0.7      // 调整参数 / Adjust parameters
    }
  }
}
```

**或使用 .env 文件 / Or use .env file:**
```bash
cp .env.example .env        # 复制示例文件 / Copy example file
# 然后编辑 .env 填入你的配置 / Then edit .env with your config
```

#### 步骤 3 / Step 3: 添加 API 密钥 / Add API Key

```bash
# 在 .env 文件中 / In .env file:
OPENAI_API_KEY=sk-your-real-api-key-here
```

**重要提示 / Important:** 
- ⚠️ 不要提交 `.env` 文件到 Git！ / Don't commit `.env` to Git!
- ✅ `.gitignore` 已经配置好了 / `.gitignore` is already configured

---

## 📋 支持的模型 / Supported Models

| 提供商 / Provider | 模型 / Models | 适用场景 / Best For |
|------------------|--------------|-------------------|
| OpenAI | gpt-4, gpt-4-turbo, gpt-3.5-turbo | 通用任务 / General tasks |
| Anthropic | claude-3-opus, claude-3-sonnet, claude-3-haiku | 长文本分析 / Long text analysis |
| Google | gemini-pro, gemini-pro-vision | 多模态任务 / Multimodal tasks |
| Local | llama-2, mistral | 离线使用 / Offline use |

---

## 🎯 常见配置场景 / Common Scenarios

### 场景 1: 我想要最强大的模型
### Scenario 1: I want the most powerful model

```json
{
  "model": {
    "provider": "openai",
    "name": "gpt-4-turbo",
    "parameters": {
      "temperature": 0.7,
      "max_tokens": 4000
    }
  }
}
```

### 场景 2: 我想要便宜且快速的模型
### Scenario 2: I want a cheap and fast model

```json
{
  "model": {
    "provider": "openai",
    "name": "gpt-3.5-turbo",
    "parameters": {
      "temperature": 0.5,
      "max_tokens": 1000
    }
  }
}
```

### 场景 3: 我想要离线本地模型
### Scenario 3: I want an offline local model

```json
{
  "model": {
    "provider": "local",
    "name": "llama-2-13b",
    "api_key": "",
    "parameters": {
      "temperature": 0.8
    }
  }
}
```

---

## ❓ 常见问题 / FAQ

### Q: 我需要哪个 API 密钥？
### Q: Which API key do I need?

A: 取决于你选择的提供商：
A: Depends on your chosen provider:
- OpenAI → `OPENAI_API_KEY`
- Anthropic → `ANTHROPIC_API_KEY`
- Google → `GOOGLE_API_KEY`
- Local → 不需要 / Not needed

### Q: 如何切换模型？
### Q: How do I switch models?

A: 只需修改 `model-config.json` 中的 `provider` 和 `name` 字段，或者修改 `.env` 文件中的 `MODEL_PROVIDER` 和 `MODEL_NAME`。

A: Just modify the `provider` and `name` fields in `model-config.json`, or modify `MODEL_PROVIDER` and `MODEL_NAME` in `.env`.

### Q: 什么是 temperature？
### Q: What is temperature?

A: 温度控制输出的随机性：
A: Temperature controls output randomness:
- 0.0-0.3: 确定性、事实性输出 / Deterministic, factual output
- 0.5-0.7: 平衡的创造力 / Balanced creativity
- 0.8-2.0: 高度创造性、多样化 / Highly creative, diverse

---

## 📚 更多信息 / More Information

- 详细说明：查看 `README.md` / Detailed docs: See `README.md`
- 使用示例：查看 `USAGE_EXAMPLES.md` / Usage examples: See `USAGE_EXAMPLES.md`
- 配置文件：`model-config.json` / Config file: `model-config.json`

---

## ✅ 完成！/ Done!

你现在可以配置和切换不同的 AI 模型了！

You can now configure and switch between different AI models!
