# awesome-dify-workflow

分享高质量的 Dify 工作流，通过一个DSL文件即可导入使用。

## 目录

### DeepGemini

DeepSeek R1 和 Gemini 2.0 的结合,实现更好的思考过程和更优质的输出
![DeepGemini流程](/imgs/DeepGemini.png)

### 长文本写作

通过生成大纲再生成具体内容的方式实现上万字的超长文本输出。
![长文本写作流程](/imgs/long-form-writing.png)

### 意图识别

根据用户意图选择性回复。
![意图识别流程](/imgs/intent-recognition.png)

### 异常处理

提前配置对应的错误处理工作流来捕获运行时的异常使用
![异常处理流程](/imgs/error-handling.png)

### simple-kimi

仿 KIMI 风格的工作流，多模态联网搜索和文件读取
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

## 贡献

欢迎提交高质量的工作流，提交方式：

1. fork 本项目
2. 提交 DSL 文件到 `DSLs` 目录下
3. 提交 PR
