---
name: llm-beian-writer
description: Draft, revise, and review Chinese generative AI service filing materials and large-model备案 documents. Use when Codex is asked to write 大模型备案材料, 生成式人工智能服务备案材料, 安全评估报告, 语料来源说明, 标注规则, 服务协议, 隐私政策要点, 测试集方案, 风险整改说明, or to check gaps in these materials.
---

# LLM Beian Writer

Use this skill to turn scattered product, model, data, and governance facts into filing-ready Chinese drafts for generative AI service备案 work.

## Operating Rules

- Treat备案写作 as compliance drafting, not legal certification. Never state that a service is compliant, approved, or备案通过 unless the user provides evidence.
- Prefer official sources, the user's company facts, and filed internal documents over third-party examples.
- Mark unknowns as `待补充` or `需确认`; do not invent model parameters, data sources, licenses, safety metrics, or regulator feedback.
- Separate `可直接写入材料` from `内部待确认事项` when drafting.
- Use formal, factual, regulator-facing Chinese. Avoid marketing language, exaggeration, or broad claims like “行业领先”.
- If the user asks for final submission material, first produce a gap checklist and ask for missing facts before polishing.

## First Questions To Resolve

When key facts are missing, ask only for the next smallest useful batch:

- 备案主体：公司全称、统一社会信用代码、联系人角色、属地。
- 服务：服务名称、入口、面向公众还是内部、文本/图片/音频/视频/API 类型。
- 模型：自研/采购/开源/混合，模型名称、版本、部署方式、供应商或开源协议。
- 数据：训练/微调/RAG/知识库来源，是否含个人信息、版权内容、境外数据。
- 安全：内容安全策略、人工审核、投诉举报、应急处置、日志留存、未成年人保护。
- 测评：测试集、红队测试、拦截策略、抽样结果、整改记录。

## Workflow

1. Identify the task type: `新备案起草`, `补充材料`, `差距审查`, `安全评估报告`, `语料/标注说明`, `用户协议/隐私条款`, or `整改回复`.
2. Load `references/material-checklist.md` for material coverage.
3. Load `references/regulatory-sources.md` when mapping claims to sources or reviewing compliance basis.
4. Use `assets/templates/common-materials.md` when the user needs a reusable draft.
5. Produce output in this order: `结论`, `可用草稿`, `待补充信息`, `风险点`, `建议附件`.
6. For reviews, use severity labels: `高`, `中`, `低`, with evidence and a practical fix.

## Drafting Standards

- Write every material around evidence: system screenshots, policies, logs, test results, data source contracts, model documentation, vendor agreements, and review records.
- For data/corpus sections, cover lawful source, IP rights, personal information basis, quality control, filtering, deduplication, labeling, and update/removal mechanism.
- For model/security sections, cover input/output controls, prohibited content handling, discrimination/bias mitigation, hallucination and accuracy controls, abuse prevention, human review, and emergency response.
- For service governance, cover user real-name or account management if applicable, user agreement, privacy notice, complaint/reporting channel, feedback SLA, minors protection, generated-content labeling if applicable, and logs.

## Output Guardrails

- Do not provide advice that circumvents regulator review.
- Do not include confidential secrets unless the user explicitly provides them for drafting.
- Do not cite an article number unless verified from an official source or a user-provided official document.
- If local/sector-specific rules may apply, say so and flag it for legal or regulator confirmation.
