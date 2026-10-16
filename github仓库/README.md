# AI UI Design Lab

> 从设计理念到多模型协作：学习、实验、验证与持续改进。

本仓库记录我对 AI 辅助 UI 设计方法的学习与实践。目标不是简单收集提示词，而是把设计理念转化为可执行、可检查、可复现的工作流。

## 项目原则

1. **来源透明**：明确区分外部来源、个人理解、AI 辅助分析和原创实验。
2. **证据优先**：最终界面以真实渲染截图、交互测试和可复现结果为依据。
3. **人类负责设计判断**：模型扩展方案、执行任务和提供批评；项目维护者负责取舍和最终验收。
4. **按需使用工具**：图像、视频和多个模型只在能产生明确价值时引入。
5. **记录失败**：记录无效提示词、失败案例、成本和修复过程。

## 内容导航

- [`SOURCES.md`](SOURCES.md)：来源、归属与使用说明
- [`docs/LEARNING_NOTES.md`](docs/LEARNING_NOTES.md)：核心设计思想与个人思考框架
- [`docs/MULTI_MODEL_WORKFLOW.md`](docs/MULTI_MODEL_WORKFLOW.md)：多模型岗位、交接与验证流程
- [`docs/MODEL_ROLE_CARDS.md`](docs/MODEL_ROLE_CARDS.md)：GPT、Codex、Claude、Gemini、Grok、DeepSeek 岗位卡
- [`docs/SETUP_AND_VALIDATION.md`](docs/SETUP_AND_VALIDATION.md)：第一次端到端接入与验收指南
- [`prompts/`](prompts/)：可复制的通用阶段提示词和模型岗位提示词
- [`skills/distinctive-ai-design/`](skills/distinctive-ai-design/)：经检查、注明来源并逐步改编的 Skill 工作区
- [`experiments/template/`](experiments/template/)：每次 UI 实验的记录模板

## 推荐工作流

`需求澄清 → 设计探索 → 人类选方向 → Design Brief → 实现 → 真实截图 → 独立评审 → 精修 → QA → 记录结果`

1. 明确产品、用户、任务和技术约束。
2. 探索 3 个结构上真正不同的设计方向。
3. 由人选择方向，并整理为设计 brief。
4. 由一个主力编码代理实现关键页面。
5. 在真实浏览器中生成桌面和移动端截图。
6. 由独立评审上下文检查截图，给出具体问题。
7. 只修复影响最大的 1–3 个问题，再重新验证。
8. 检查交互、响应式、键盘操作、对比度与错误状态。
9. 保存证据，比较“使用 Skill”与“不使用 Skill”的结果。

## 归属说明

本仓库是个人学习、分析和实验项目。外部文章、视频、评论区分享的 Skill 及其作者仍归原作者所有。请阅读 [`SOURCES.md`](SOURCES.md)，并在纳入第三方代码或文件前核对其许可证及归属要求。

## 当前状态

初始模板尚不代表已经完成模型接入或端到端验证。所有未实际运行的步骤都应标记为“待验证”，不得写成“测试通过”。
