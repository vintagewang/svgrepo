# 模型配置使用示例 / Model Configuration Usage Examples

## 示例 1: 使用 OpenAI GPT-4 / Example 1: Using OpenAI GPT-4

### 配置文件方式 / Configuration File Method

```json
{
  "model": {
    "provider": "openai",
    "name": "gpt-4",
    "api_key": "${OPENAI_API_KEY}",
    "parameters": {
      "temperature": 0.7,
      "max_tokens": 2000
    }
  }
}
```

### 环境变量方式 / Environment Variable Method

```bash
MODEL_PROVIDER=openai
MODEL_NAME=gpt-4
MODEL_TEMPERATURE=0.7
MODEL_MAX_TOKENS=2000
OPENAI_API_KEY=sk-your-key-here
```

---

## 示例 2: 使用 Anthropic Claude / Example 2: Using Anthropic Claude

### 配置文件方式 / Configuration File Method

```json
{
  "model": {
    "provider": "anthropic",
    "name": "claude-3-opus",
    "api_key": "${ANTHROPIC_API_KEY}",
    "parameters": {
      "temperature": 0.5,
      "max_tokens": 4000
    }
  }
}
```

### 环境变量方式 / Environment Variable Method

```bash
MODEL_PROVIDER=anthropic
MODEL_NAME=claude-3-opus
MODEL_TEMPERATURE=0.5
MODEL_MAX_TOKENS=4000
ANTHROPIC_API_KEY=sk-ant-your-key-here
```

---

## 示例 3: 使用本地模型 / Example 3: Using Local Model

### 配置文件方式 / Configuration File Method

```json
{
  "model": {
    "provider": "local",
    "name": "llama-2-13b",
    "api_key": "",
    "parameters": {
      "temperature": 0.8,
      "max_tokens": 1000,
      "context_length": 4096
    }
  }
}
```

### 环境变量方式 / Environment Variable Method

```bash
MODEL_PROVIDER=local
MODEL_NAME=llama-2-13b
MODEL_TEMPERATURE=0.8
MODEL_MAX_TOKENS=1000
```

---

## 快速切换模型 / Quick Model Switching

你可以通过修改配置文件快速切换不同的模型：

You can quickly switch between different models by modifying the configuration:

```bash
# 切换到 GPT-3.5 (更快、更便宜)
# Switch to GPT-3.5 (faster, cheaper)
MODEL_NAME=gpt-3.5-turbo

# 切换到 Claude Sonnet (平衡性能和成本)
# Switch to Claude Sonnet (balanced performance and cost)
MODEL_PROVIDER=anthropic
MODEL_NAME=claude-3-sonnet

# 切换到 Gemini (Google 的模型)
# Switch to Gemini (Google's model)
MODEL_PROVIDER=google
MODEL_NAME=gemini-pro
```

---

## 参数调优建议 / Parameter Tuning Recommendations

### 创意任务 / Creative Tasks
```json
{
  "temperature": 0.9,
  "top_p": 0.95,
  "frequency_penalty": 0.5
}
```

### 分析任务 / Analytical Tasks
```json
{
  "temperature": 0.3,
  "top_p": 0.9,
  "frequency_penalty": 0.0
}
```

### 代码生成 / Code Generation
```json
{
  "temperature": 0.2,
  "top_p": 0.95,
  "presence_penalty": 0.0
}
```

### 对话聊天 / Conversational Chat
```json
{
  "temperature": 0.7,
  "top_p": 1.0,
  "frequency_penalty": 0.3,
  "presence_penalty": 0.6
}
```
