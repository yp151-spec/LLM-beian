# LLM-beian

这个仓库用于沉淀“生成式人工智能服务备案 / 大模型备案”材料写作的 Codex skill、模板和参考清单。

当前包含：

- `skills/llm-beian-writer/`：用于日常起草、补充、审查备案材料的 Codex skill。
- `skills/llm-beian-writer/references/`：材料清单、写作流程、法规来源、客户材料通用模式，以及大模型备案/算法备案边界。
- `skills/llm-beian-writer/assets/templates/`：常用材料草稿模板。

## 使用方式

在 Codex 中可以按 GitHub 路径安装这个 skill：

`yp151-spec/LLM-beian` -> `skills/llm-beian-writer`

安装后重启 Codex，然后用类似下面的请求触发：

- “帮我起草大模型备案安全评估报告”
- “审查这份生成式人工智能服务备案材料缺什么”
- “根据我的产品信息生成语料来源说明和标注规则”
- “帮我写网信办补充材料回复”
- “先判断这是大模型备案还是算法备案，再帮我列材料清单”

注意：备案材料具有属地差异和实时变化，本仓库用于提高起草效率，不替代律师、合规负责人或属地网信办的正式确认。
