# awesome-dify-workflow

分享高质量的 Dify 工作流，通过一个 DSL 文件即可导入使用。

当前仓库收录 **74** 个可导入 DSL，主要来自开源社区高星项目与官方 AWS 示例。建议使用 **Dify 0.13.0+** 导入；含 Agent / MCP 节点的流程请尽量用最新版 Dify。

导入方式：Dify 控制台 → 创建应用 → 导入 DSL 文件。导入后按需替换模型、工具授权和 API Key。

## 目录

- [精选](#精选)
- [Agent 与深度研究](#agent-与深度研究)
- [翻译](#翻译)
- [内容创作](#内容创作)
- [搜索、RAG 与知识库](#搜索rag-与知识库)
- [数据处理与可视化](#数据处理与可视化)
- [代码与开发](#代码与开发)
- [聊天与记忆](#聊天与记忆)
- [AWS 生态](#aws-生态)
- [自动化与集成](#自动化与集成)
- [来源](#来源)
- [贡献](#贡献)

## 精选

### DeepGemini

DeepSeek R1 和 Gemini 2.0 的结合，实现更好的思考过程和更优质的输出。

![DeepGemini流程](/imgs/DeepGemini.png)

### 长文本写作

通过生成大纲再生成具体内容的方式实现上万字的超长文本输出。

![长文本写作流程](/imgs/long-form-writing.png)

### 意图识别

根据用户意图选择性回复。

![意图识别流程](/imgs/intent-recognition.png)

### 异常处理

提前配置对应的错误处理工作流来捕获运行时的异常。

![异常处理流程](/imgs/error-handling.png)

### simple-kimi

仿 KIMI 风格的工作流，多模态联网搜索和文件读取。

![simple-kimi流程](/imgs/simple-kimi.png)

### deep-research

一个深度研究工作流，通过联网搜索和文件读取，生成详细的研究报告。

![deep-research流程](/imgs/deep-research.png)

### document chat

一个通过知识库进行文档问答的基础模板，适合快速搭建 RAG 聊天工作流。

![document chat流程](/imgs/document-chat-template.jpg)

### 搜索大师

通过 SearXNG 进行联网搜索，再用 Jina 获取网页内容并汇总回答。

![搜索大师流程](/imgs/search-master.jpg)

### translation_workflow

基于 Agentic Workflow 的翻译工具，按输入语言、目标语言、国家和原文生成更细致的翻译结果。

![translation_workflow流程](/imgs/translation-workflow.jpg)

### SEO Slug Generator

将标题或正文转换为简洁、语义清晰的英文 URL slug，适合博客和内容站发布前使用。

![SEO Slug Generator流程](/imgs/seo-slug-generator.jpg)

### 三语一致性检查

用于检查和优化三种语言版本之间的表达一致性，适合多语言内容审核。

![三语一致性检查流程](/imgs/language-consistency-checker.jpg)

## Agent 与深度研究

| 文件 | 说明 |
| --- | --- |
| `AgentFlow.yml` | 通用 Agent Chatflow，适合作为工具调用型对话入口。 |
| `Agent工具调用.yml` | Dify 1.0 Agent 节点示例，用 Function Calling 选择工具并回复。 |
| `Demo-tod_agent.yml` | 面向多轮对话的 Agent 策略 Demo，强调上下文理解和信息收集。 |
| `旅行Demo.yml` | 旅行信息收集示例：工具调用 + 把对话历史写入会话变量。 |
| `Deep Researcher On Dify .yml` | Open Deep Research 在 Dify 上的复现，适合长链路调研。 |
| `llm2o1.cn.yml` | 任务拆解 → 逐步执行 → 归纳总结，用普通 LLM 模拟更强推理。 |
| `思考助手.yml` | 辅助思考与规划的对话工作流。 |
| `MCP.yml` | MCP 工具调用 Chatflow 示例。 |
| `MCP-amap.yml` | 通过 MCP Agent 策略调用高德地图在线服务。 |
| `Artifact.yml` | 配合 Artifacts 插件渲染 LLM 生成的 HTML / Canvas。 |

## 翻译

| 文件 | 说明 |
| --- | --- |
| `中译英.yml` | 直译 → 反思 → 意译，产出更高质量英文。 |
| `DuckDuckGo翻译+LLM二次翻译.yml` | 先用翻译引擎打底，再用 LLM 润色，节省 Token。 |
| `宝玉的英译中优化版.yml` | 科技文章英译中优化版，强化提示词和 XML 标签。 |
| `全书翻译.yml` | 切分长文本后在迭代器中翻译，适合整书/长文档。 |
| `json_translate.yml` | 解析 JSON 中需翻译字段，迭代翻译后保持原结构。 |
| `term_based_translation_workflow.yml` | 带术语表约束的翻译流程，适合专有名词场景。 |

## 内容创作

| 文件 | 说明 |
| --- | --- |
| `标题党创作.yml` | 爆款标题 / 网文标题生成。 |
| `文章仿写-单图_多图自动搭配.yml` | 输入网页 URL，完成文章仿写并自动配图。 |
| `Text to Card Iteration.yml` | 迭代生成小红书风格图文卡片。 |
| `Dify 运营一条龙.yml` | 小红书 / 抖音 / 微博 / B 站多平台文案与封面思路示例。 |
| `dify_course_demo.yml` | 自动化生成全套教程大纲与内容。 |
| `春联生成器.yml` | 生成春联；字体依赖本机环境，可按需修改。 |
| `春联生成器 (“福”到了版本).yml` | 春联生成器的“福”字增强版本。 |
| `svg_designer.yml` | 创意 Logo / SVG 设计生成。 |
| `generate_image_video.yml` | 文生图 / 视频内容生成示例。 |
| `edu_question_gen.yml` | 教育场景出题组卷。 |

## 搜索、RAG 与知识库

| 文件 | 说明 |
| --- | --- |
| `Jina Reader Jinja.yml` | 基于搜索 + Jina 读取网页的问答流程。 |
| `图文知识库.yml` | 知识库检索后输出图配文效果的示例。 |
| `basic_rag_sample.yml` | 基础 RAG 工作流模板。 |
| `bedrock_knowledge_retreival+Chatbot .yml` | Bedrock Knowledge 检索 + Chatbot。 |
| `s3_rag.yml` | 基于 S3 文档的 RAG 流程。 |
| `rag_based_bot_with_tts.yml` | RAG 机器人，支持语音播报。 |
| `rag_based_chatbot_for_nextcloud.yml` | Nextcloud 网盘 + 知识库问答。 |
| `Sagemaker-Bge-Rerank.yml` | SageMaker BGE Rerank 重排序示例。 |
| `opensearch_img_search.yml` | OpenSearch 图文检索。 |

## 数据处理与可视化

| 文件 | 说明 |
| --- | --- |
| `json-repair.yml` | 修复大模型输出的不合法 JSON。 |
| `File_read.yml` | 用 sandbox 读取并解析上传文件（如 pandas 读 CSV）。 |
| `runLLMCode.yml` | LLM 生成代码后通过 HTTP/sandbox 执行，适合 CSV 分析。 |
| `matplotlib.yml` | matplotlib 绘图并输出 base64 图片。 |
| `chart_demo.yml` | 在回复中渲染 charts 图表。 |
| `jieba.yml` | jieba 中文分词示例。 |

## 代码与开发

| 文件 | 说明 |
| --- | --- |
| `Python Coding Prompt.yml` | 通过对话生成 Python 代码。 |
| `Claude3 Code Translation.yml` | 不同编程语言之间的代码翻译。 |
| `code_interpreter_demo.yml` | 代码解释器 / 沙箱执行示例。 |
| `腾讯云SubtitleInfo.yml` | 代码节点示例：腾讯云字幕授权信息加密与请求。 |
| `eks_upgrade_planning.yml` | EKS 升级规划助手，适合基础设施变更评估。 |

## 聊天与记忆

| 文件 | 说明 |
| --- | --- |
| `根据用户的意图进行回复.yml` | 先做意图判定，再走不同分支并风格化回复。 |
| `Form表单聊天Demo.yml` | 对话框内表单登录后再访问模型。 |
| `记忆测试.yml` | 短期记忆 + CoT 思维链，可按上下文选择回复。 |
| `AgentCore-Memory-1.yml` | AgentCore Memory 示例：宠物管家 Bob。 |
| `AgentCore-Memory-2.yml` | AgentCore Memory 示例：护理员 Alice。 |
| `瞎说新语v2.yml` | 轻松闲聊风格的对话应用。 |
| `完蛋！我被LLM包围了！ .yml` | 和模型博弈、诱导其按指令回答的趣味流程。 |
| `完蛋！我被LLM包围了！（战绩排行版）.yml` | 上一游戏的战绩排行版本。 |

## AWS 生态

以下流程来自 [aws-samples/dify-aws-tool](https://github.com/aws-samples/dify-aws-tool)，导入后需要配置对应的 AWS / Bedrock / SageMaker 插件。

| 文件 | 说明 |
| --- | --- |
| `ASR_Transcribe.yml` | Amazon Transcribe 语音转写。 |
| `apply_guardrails.yml` | 使用 Guardrail 对文本做安全审查。 |
| `chat-with-browser.yml` | 远程浏览器交互（AgentCore Browser）。 |
| `mcp_server_integration.yml` | 在工作流中集成 MCP Server。 |
| `LLM-Finetuning-Dataflow-dify.yml` | 输入网页后做内容仿写 / 改写的数据流示例。 |

## 自动化与集成

| 文件 | 说明 |
| --- | --- |
| `daily-news-slack.yml` | 定时抓取新闻并推送到 Slack 频道。 |
| `slack-news-researcher.yml` | Slack 新闻调研 Agent。 |
| `confluence-to-feishu.yml` | 将 Confluence 内容同步到飞书。 |
| `小支付-DEMO.yml` | 工作流内接入收款能力的 Demo。 |

## 来源

本仓库 DSL 整理自以下可再分发的开源项目，并保留各自许可证：

| 来源 | 许可证 | 说明 |
| --- | --- | --- |
| [svcvit/Awesome-Dify-Workflow](https://github.com/svcvit/Awesome-Dify-Workflow) | MIT | 社区最全的 Dify DSL 合集之一 |
| [aws-samples/dify-aws-tool](https://github.com/aws-samples/dify-aws-tool) | MIT-0 | AWS 官方示例工作流 |
| [ghostviper/dify-workflow](https://github.com/ghostviper/dify-workflow) | Apache-2.0 | 标题党 / 文章仿写等创作流 |
| [Petrus-Han/dify-usecase-playground](https://github.com/Petrus-Han/dify-usecase-playground) | Apache-2.0 | 定时新闻、知识库同步等生产向示例 |

更多公开合集（未直接拷贝，因仓库未声明许可证）：

- [wwwzhouhui/dify-for-dsl](https://github.com/wwwzhouhui/dify-for-dsl)
- [BannyLon/DifyAIA](https://github.com/BannyLon/DifyAIA)
- [Dify Marketplace](https://marketplace.dify.ai/templates)（官方模板市场，需登录后下载）

## 贡献

欢迎提交高质量的工作流，提交方式：

1. fork 本项目
2. 提交 DSL 文件到 `DSLs` 目录下
3. 在本 README 对应分类中补充一行说明
4. 提交 PR
