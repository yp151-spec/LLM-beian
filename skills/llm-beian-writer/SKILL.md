---
name: llm-beian-writer
description: Draft, revise, and review Chinese generative AI service filing materials and large-model备案 documents. Use when Codex is asked to write or check 大模型备案材料, 生成式人工智能服务备案材料, 大语言模型上线备案表, 登记备案表, 安全评估报告, 调用已备案模型情况说明, 内容安全管理制度, 语料来源说明, 语料标注规则, 拦截关键词列表, 评估测试题, 测试账号/API接口材料, 服务协议, 隐私政策, 补充材料回复, or when the user needs to distinguish 大模型备案 from 算法备案.
---

# LLM Beian Writer

Use this skill to turn scattered product, model, data, security, and governance facts into filing-ready Chinese drafts for generative AI service备案 work.

## Operating Rules

- Treat备案写作 as compliance drafting, not legal certification. Never state that a service is compliant, approved, or备案通过 unless the user provides evidence.
- First classify the work as `大模型上线备案`, `调用已备案大模型登记/备案`, `算法备案`, `深度合成/生成合成标识`, or `不确定`. Load `references/filing-boundary.md` whenever the boundary matters.
- Do not mix deliverables: 大模型备案材料 are not the same as 算法备案的自评估报告、拟公示算法机制机理内容、算法安全责任人材料.
- Prefer official sources, the user's company facts, and filed internal evidence over third-party examples.
- Mark unknowns as `待补充` or `需确认`; do not invent model parameters, data sources, licenses,备案号, pass rates, test counts, or regulator feedback.
- Separate `可直接写入材料` from `内部待确认事项` when drafting.
- Generalize from prior client materials. Do not copy client-specific names, screenshots, test questions, contracts, or sensitive examples unless the user explicitly asks to work on that client file.
- Use formal, factual, regulator-facing Chinese. Avoid marketing language, exaggeration, or broad claims like “行业领先”.
- If the user asks for final submission material, first produce a gap checklist and ask for missing facts before polishing.

## First Questions To Resolve

When key facts are missing, ask only for the next smallest useful batch:

- 备案路径：自研/微调大模型上线备案，调用已备案大模型登记/备案，新产品/新功能上线，还是算法备案。
- 备案主体：公司全称、统一社会信用代码、法定代表人、安全评估负责人、联系人、属地、行业主管部门。
- 服务：服务名称、入口、服务形态、服务对象、公众/内部/ToB/ToG、是否面向未成年人、服务领域和边界。
- 模型：自研/第三方/开源/微调/调用已备案模型，模型名称、版本、参数规模、基座模型、备案单位、备案号、调用方式、部署地点。
- 算力与系统：训练/推理服务器、GPU、第三方云平台、部署区域/IP、系统流程图、模型更新和回滚机制。
- 数据：训练、微调、RAG、知识库来源；开源/自采/商业数据；授权、robots、合同、个人信息、版权、境外数据情况。
- 安全：内容安全策略、非法内容拦截标准、关键词库、分类模型、人工审核、投诉举报、应急处置、日志留存、未成年人保护、生成合成内容标识。
- 测评：评估测试题库、应拒答/非拒答/应答题、红队测试、拦截策略、抽样方法、模型返回、研判结果、整改记录。
- 附件：服务协议、隐私政策、内容安全管理制度、语料标注规则、测试账号/API接口、授权合同、开源许可、数据采集记录。

## Workflow

1. Identify the filing route and boundary. If there is algorithm备案 language, load `references/filing-boundary.md`.
2. Load `references/material-checklist.md` for material coverage and required evidence.
3. Load `references/client-material-patterns.md` when drafting a full package, organizing folders, or checking common omissions from real-world materials.
4. Load `references/regulatory-sources.md` when mapping claims to legal/standard sources or reviewing source hierarchy.
5. Use `assets/templates/common-materials.md` when the user needs reusable draft text.
6. Produce output in this order: `结论`, `适用备案路径`, `可用草稿/修改稿`, `待补充信息`, `风险点`, `建议附件`.
7. For reviews, use severity labels: `高`, `中`, `低`, with evidence and a practical fix.

## Drafting Standards

- Write every material around evidence: signed/sealed forms, system screenshots, policies, logs, test results, data source contracts, model/vendor documentation, open-source licenses, data collection records, training records, complaint channels, and review records.
- For data/corpus sections, cover lawful source, IP rights, personal information basis, quality control, filtering, deduplication, labeling, training/test split, update/removal mechanism, and whether data is open-source, self-collected, commercial, or user-uploaded.
- For model/security sections, cover input/output controls, prohibited content handling, discrimination/bias mitigation, hallucination and accuracy controls, abuse prevention, human review, monitoring, incident response, model iteration, and service continuity.
- For test materials, distinguish `应拒答题库`, `非拒答题库`, `应答题库`, vertical-domain tests, and categories such as IP/trade secret, discrimination, accuracy/reliability, illegal/harmful content, and scenario-specific risk.
- For service governance, cover account/real-name rules if applicable, user agreement, privacy notice, complaint/reporting channel, feedback SLA, opt-out of using user input for training, minors protection, generated-content labeling if applicable, and logs.
- For folder/package work, preserve local naming conventions and produce both Word/PDF requirements where required, but never place test accounts/API keys inside submission folders unless the specific path requests them.

## Output Guardrails

- Do not provide advice that circumvents regulator review.
- Do not include confidential secrets unless the user explicitly provides them for drafting.
- Do not cite an article number unless verified from an official source or a user-provided official document.
- If local/sector-specific rules may apply, say `属地口径待确认` or `行业主管部门口径待确认`.
- If the task is actually algorithm备案, say so clearly and keep it separate from 大模型备案 deliverables.
