# Client Material Patterns

This reference distills reusable patterns observed across local filing packages. It is not a source of legal authority and must not be copied verbatim into client drafts. Use it to structure work, check gaps, and avoid mixing 大模型备案 with 算法备案.

## Folder And Packaging Patterns

### Full large-model online filing

Common folder order:

1. `0 生成式人工智能（大语言模型）上线备案表`
2. `1 附件1-安全评估报告`
3. `2 附件2-模型服务协议`
4. `3 附件3-语料标注规则`
5. `4 附件4-拦截关键词列表`
6. `5 附件5-评估测试题`
7. `6 附件6-关于英伟达断供后大模型迭代发展的考虑`
8. `7 附件7-其他佐证文档` or `8 附件8-其他佐证文档` depending on local template

Common package notes:

- The root package may say not to include test account or API interface files inside the submission folder.
- Delete all `说明.txt` helper files before final delivery.
- Word and PDF are commonly both required for form, safety report, service agreement/privacy, labeling rules, and special addenda.
- Other evidence folders may accept Word/PDF proof, but should not include passwords, API keys, or test-channel secrets unless requested.

### Calling a filed model / registration route

Common folder order:

1. `0 生成式人工智能（大语言模型）登记备案表` or `调用已备案大模型上线备案表`
2. `1 附件1-调用已备案大模型情况说明及相关证明材料`
3. `2 附件2-产品服务协议（产品使用协议、隐私保护政策）`
4. `3 附件3-内容安全管理制度`
5. `4 附件4-拦截关键词库`
6. `5 附件5-评估测试题`
7. `6 测试通道（测试账号及API接口）` if requested
8. `7 其他（若有）`

Key difference: the proof focus shifts to filed model name, filing entity, filing number, call/deployment method, authorization/contract, product safety management, and test evidence.

## Information Collection Patterns

Large-model information collection forms commonly ask for:

- Basic subject information: company name, legal representative, safety assessment负责人, phone, office address, company nature, superior company, industry主管部门.
- Service information: model/service name, function, service content, service method, target users, minors, service scenarios, service field, public-test date, service channel.
- User access: registration/login, agreement/privacy acceptance, screenshots, account cancellation, complaint/report path.
- Personal information: type, quantity, purpose, retention, consent, deletion/correction path.
- Model source: self-developed, fine-tuned from third-party base, calling filed model, open-source/commercial authorization.
- Compute resources: training and inference server brand/model/count, GPU brand/model/count, cloud provider, platform/server location, IP.
- Model mechanism: architecture, training framework, process topology, input/output safety controls, update and rollback.
- Algorithm备案 status may appear as a field in the form; record it factually, but do not convert the task into algorithm备案 unless the deliverable asks for that track.

## Safety Report Patterns

Safety reports usually organize around:

- `语料安全评估`: corpus scale, source, labeling quantity, labeler information, label rules, legality, personal information, IP disputes, risk prevention.
- `模型安全评估`: generated-content safety, IP/trade-secret issues, commercial ethics, discrimination, transparency, accuracy, reliability, service-type-specific risk.
- `安全措施评估`: target users, personal information, user rights requests, generated-content labels for image/video/multimodal output, complaints, service agreement, monitoring.
- `总体结论`: whether to recommend launch, major residual risks, mitigation, post-launch risk forecast, response capability.

Common evaluation language should be evidence-backed:

- `评估方法`: manual sampling, keyword sampling, classifier/model sampling, red-team tests, vertical-domain tests.
- `判断标准`: category rules, refusal/answer criteria, pass/fail criteria.
- `评估结果`: sample size, pass rate, block/refusal rate, failure count,整改 before/after.

## Keyword And Test Bank Patterns

Keyword library:

- Keep it full, latest, classified, and editable.
- Typical columns: `关键词`, `一级分类`, `二级分类`.
- It may contain sensitive entries; do not quote raw keywords in ordinary summaries.

Evaluation test bank:

- Keep it full, latest, classified, and editable.
- Typical columns: `序号`, `测试题`, `一级分类`, `二级分类`, `模型返回/模型回答`, `研判结果/是否合格`.
- Typical sheets/categories: IP/trade secret, discrimination, accuracy/reliability, should-refuse, non-refusal, should-answer, vertical-domain scenario tests.
- Do not expose sensitive prompt examples in public-facing drafts; describe categories, counts, and aggregate results.

## Content Safety Management System Pattern

When the route asks for `内容安全管理制度`, include:

- Purpose and scope.
- Management principles: legality, accuracy/reliability, positive values, consistency, privacy.
- Content review flow: content creation/input, submission, machine review, human review, escalation, record keeping.
- Illegal-content interception standards:
  - Violations of socialist core values and laws/regulations.
  - Discriminatory content.
  - Commercial illegalities, IP infringement, trade secret leakage, monopoly/unfair competition.
  - Other prohibited or harmful content.
- Monitoring and handling: real-time monitoring, complaint/reporting, violation disposal.
- Personnel training and management: training system, examination, roles, permission levels.
- Emergency response: content safety incidents, public opinion incidents, shutdown/degradation,整改.

## Evidence Checklist Patterns

Useful attachments often include:

- Service screenshots: registration/login, agreement and privacy acceptance, public service page, complaint/report entrance, generated-content labeling, opt-out of input-for-training.
- Model proof: filed model proof,备案号, vendor authorization, commercial contract, open-source license, model card or technical documentation.
- Data proof: open-source license pages, commercial data contracts, self-collection logs, robots review, data sampling records, data quality report.
- Labeling proof: label manual, labeler training, assessment records, role separation, quality review.
- Safety proof: keyword library, classifier strategy, safety prompts/rules, machine/human review screenshots, incident handling records.
- Test proof: test bank, aggregate metrics, failure cases summarized,整改 records.
- Continuity proof: backup, disaster recovery, compute migration plan, model update/rollback record.

## Drafting Caveats

- Write from the user's verified facts, not from observed client examples.
- If the user asks to work from a prior client package, confirm whether client-specific names, screenshots, contracts, or test examples should be preserved or anonymized.
- Treat local forms as practice patterns. If a form conflicts with current official guidance or local regulator feedback, follow the current official/local requirement and flag the conflict.
