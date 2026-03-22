# iBot Synthetic Intelligence — OpenClaw Integration

## Overview

This skill connects OpenClaw with the iBot Synthetic Intelligence platform,
enabling access to 136+ AI skills, 14 local Ollama models, and multi-provider
intelligence routing.

## Capabilities

### Local AI Models (Ollama)
- **Vision:** gemma3:4b, gemma3:12b, gemma3:27b, llama4:scout
- **Code:** qwen2.5-coder:32b
- **Chat:** qwen3:32b, llama3.3:70b, mistral:7b, deepseek-r1:7b
- **Embedding:** nomic-embed-text

### Cloud Providers
- AWS Bedrock (Claude Sonnet 4)
- DeepSeek Chat
- OpenAI GPT-4o
- Cloudflare AI Gateway

### Skills
- Web search and URL fetching
- Local file system access (read/write/PDF)
- Shell command execution
- Code generation and review
- Image analysis via Ollama vision
- Pipeline composition and automation
- GitHub deploy (clone/commit/push)

## Configuration

```env
# Add to .env
IBOT_GATEWAY_URL=ws://localhost:18789/gateway
IBOT_TOKEN=your-token-here
OLLAMA_URL=http://127.0.0.1:11434
OLLAMA_MODEL=gemma3:4b
```

## Usage

```bash
# In OpenClaw, use iBot skills:
openclaw skill ibot-search "latest AI news"
openclaw skill ibot-vision /path/to/image.png
openclaw skill ibot-code "write a REST API in Python"
```
