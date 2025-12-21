# AI-Vanguard

[![Release](https://img.shields.io/github/v/release/kk12-30/AI-Vanguard)](https://github.com/kk12-30/AI-Vanguard/releases)

AI-Vanguard 是一款基于 AI 的自动化安全测试工具，旨在帮助用户快速进行网络安全评估和渗透测试。它集成了多种安全工具，并通过 AI 智能分析测试结果，提供详细的报告和建议。

## 特性

- **AI 驱动的自动化测试**：利用 AI 技术自动分析目标，制定测试策略，并执行多轮迭代测试。
- **多工具集成**：支持 Nmap、Httpx、Nuclei、Subfinder、SQLMap 等多种安全测试工具。
- **智能报告生成**：AI 自动生成详细的测试报告，包括发现的问题和下一步计划。
- **用户友好界面**：基于 Wails 的现代化桌面应用，提供直观的操作体验。
- **自定义配置**：支持自定义工具路径、API 密钥和测试参数。

## 截图

![AI-Vanguard 界面](https://github.com/kk12-30/AI-Vanguard/blob/main/Screen1.png)

## 配置

⚙️ 首次运行后，应用会在运行目录生成 `config.yaml`。您也可以在应用的"设置"界面中修改配置。

### 核心配置示例 (`config.yaml`)

```yaml
openai:
  api_key: sk-xxxxxxxxxxxx  # 您的 API 密钥
  base_url: https://api.siliconflow.cn/v1  # API 端点
  model: deepseek-ai/DeepSeek-V3.2  # 使用的模型
  max_total_tokens: 120000  # 最大 token 数
agent:
  max_iterations: 10  # 最大自动迭代次数
tools:
  - name: nmap
    command: nmap.exe
    path: Tools/nmap/nmap.exe  # 支持自定义完整路径
    # 其他参数配置
```

## 使用

1. 启动应用后，在聊天界面输入您的安全测试需求，例如："扫描 192.168.1.1 的开放端口"。
2. AI 将自动分析请求，选择合适的工具并执行测试。
3. 测试过程中，实时查看工具输出和 AI 分析结果。
4. 测试完成后，AI 会生成详细的报告，包含发现的问题和建议。
5. 如果需要终止测试，点击"终止"按钮，AI 会立即生成当前测试的总结报告。

## 贡献

欢迎提交 Issue 和 Pull Request 来帮助改进 AI-Vanguard！
