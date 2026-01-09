# svgrepo

## AI模型配置 / AI Model Configuration

### 中文说明

是的，你可以设置背后使用的AI模型！本仓库支持配置多种AI模型。

#### 配置方法

1. **使用配置文件** (`model-config.json`)
   - 打开 `model-config.json` 文件
   - 修改 `provider` 字段选择模型提供商：
     - `openai` - OpenAI (GPT-4, GPT-3.5等)
     - `anthropic` - Anthropic (Claude系列)
     - `google` - Google (Gemini系列)
     - `local` - 本地模型 (Llama, Mistral等)
   - 修改 `name` 字段选择具体模型
   - 配置API密钥和参数

2. **使用环境变量** (`.env`)
   - 复制 `.env.example` 为 `.env`
   - 填写你的API密钥
   - 设置 `MODEL_PROVIDER` 和 `MODEL_NAME`
   - 调整模型参数（温度、最大令牌数等）

#### 支持的模型

- **OpenAI**: gpt-4, gpt-4-turbo, gpt-3.5-turbo
- **Anthropic**: claude-3-opus, claude-3-sonnet, claude-3-haiku
- **Google**: gemini-pro, gemini-pro-vision
- **本地模型**: llama-2-7b, llama-2-13b, mistral-7b

#### 参数说明

- `temperature` (0.0-2.0): 控制输出的随机性，值越高越随机
- `max_tokens`: 生成的最大令牌数
- `top_p` (0.0-1.0): 核采样参数
- `frequency_penalty` (-2.0-2.0): 降低重复内容的频率
- `presence_penalty` (-2.0-2.0): 鼓励模型谈论新主题

---

### English Instructions

Yes, you can configure the AI model used behind the scenes! This repository supports configuration of multiple AI models.

#### Configuration Methods

1. **Using Configuration File** (`model-config.json`)
   - Open the `model-config.json` file
   - Modify the `provider` field to select a model provider:
     - `openai` - OpenAI (GPT-4, GPT-3.5, etc.)
     - `anthropic` - Anthropic (Claude series)
     - `google` - Google (Gemini series)
     - `local` - Local models (Llama, Mistral, etc.)
   - Modify the `name` field to select a specific model
   - Configure API keys and parameters

2. **Using Environment Variables** (`.env`)
   - Copy `.env.example` to `.env`
   - Fill in your API keys
   - Set `MODEL_PROVIDER` and `MODEL_NAME`
   - Adjust model parameters (temperature, max tokens, etc.)

#### Supported Models

- **OpenAI**: gpt-4, gpt-4-turbo, gpt-3.5-turbo
- **Anthropic**: claude-3-opus, claude-3-sonnet, claude-3-haiku
- **Google**: gemini-pro, gemini-pro-vision
- **Local Models**: llama-2-7b, llama-2-13b, mistral-7b

#### Parameter Descriptions

- `temperature` (0.0-2.0): Controls output randomness, higher is more random
- `max_tokens`: Maximum number of tokens to generate
- `top_p` (0.0-1.0): Nucleus sampling parameter
- `frequency_penalty` (-2.0-2.0): Reduces repetition of content
- `presence_penalty` (-2.0-2.0): Encourages the model to talk about new topics

---

## BYOC Diagrams

This repository also contains diagrams for Bring Your Own Cloud (BYOC) architecture.