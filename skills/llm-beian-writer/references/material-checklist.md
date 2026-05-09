# Material Checklist

This checklist is for drafting and gap review. Actual filing portals and local regulators may request different names, formats, or attachments.

## 0. First Classify The Filing Route

- `大模型上线备案`: self-developed, fine-tuned, new product, or original product新增生成式AI功能 that provides generative AI service.
- `调用已备案大模型登记/备案`: product/service mainly calls a model that has already filed, often requiring a registration form, proof of the filed model, content safety management, keywords, tests, and service governance.
- `算法备案`: internet information service algorithm filing. Keep separate from large-model备案. See `filing-boundary.md`.
- `深度合成/生成合成标识`: may overlap with algorithm备案 or generated-content labeling duties; do not treat it as the same document set as 大模型备案.

## 1. Common Full Online Filing Package

Observed package patterns commonly use the following structure:

- `0 生成式人工智能（大语言模型）上线备案表`
  - Word form.
  - Signed/sealed PDF when required.
  - Cover page and voluntary commitment page often need legal representative and safety assessment负责人 signatures and company seal.
  - Classification model information if the form asks for it.
- `1 附件1-安全评估报告`
  - Word and PDF.
  - Should cover corpus safety, model safety, safety measures, and overall conclusion.
- `2 附件2-模型服务协议`
  - `附件2.1 模型服务协议` or product service agreement.
  - `附件2.2 隐私保护政策`.
  - Word and PDF where required.
- `3 附件3-语料标注规则`
  - Word and PDF.
  - If no corpus/labeling is involved, mark the folder and material as `不涉及`, with reasons.
- `4 附件4-拦截关键词列表`
  - Editable Excel, full/latest keyword library.
  - Recommended columns: `关键词`, `一级分类`, `二级分类`; separate sheets are acceptable for categories.
- `5 附件5-评估测试题`
  - Editable Excel, full/latest self-test question bank.
  - Include test prompt, risk category, model response, and judgement result.
- `6 附件6-关于英伟达断供后大模型迭代发展的考虑`
  - Word and PDF if requested by local template.
  - Discuss compute continuity, domestic/alternative adaptation, evaluation before migration, and risk control.
- `7 附件7-其他佐证文档`
  - Useful proof such as contracts, open-source licenses, data source records, data collection records, authorization letters, model/vendor proof, project approval documents.
  - Do not place test account or API secret materials here unless the specific submission route requests it.

## 2. Calling Filed Model / Registration Package

For products that call an already filed model, the package often shifts from full corpus/model training proof to service, model-call proof, and content safety operation:

- `0 登记备案表` or `调用已备案大模型上线备案表`.
- `1 调用已备案模型情况说明及相关证明材料`.
  - Model name, filing entity,备案号, call method, deployment method, use scenario.
  - Proof such as commercial contract, authorization, service order, or vendor documentation.
- `2 产品服务协议（产品使用协议、隐私保护政策）`.
- `3 内容安全管理制度`.
  - Must include illegal-content interception standards when requested.
- `4 拦截关键词库`.
  - Full/latest/editable/classified keyword library.
- `5 评估测试题`.
  - Full/latest/editable/classified self-test question bank.
- `6 测试通道（测试账号及API接口）` if requested separately.
- `7 其他（若有）`.

## 3. Test Channel And API Materials

Keep test-channel documents separate from ordinary submission attachments when the template says so.

- Test account without added safety strategy: shows baseline product access when required.
- Test account with added safety strategy: shows actual safety-control service route.
- API specification for text large model service:
  - Stable long-term endpoint.
  - Fixed authorization method, not time-dynamic if the testing spec forbids it.
  - Request/response JSON format that matches the regulator/testing body's schema.
  - Non-stream and stream behavior documented.
  - Error behavior documented.
- Include company name, product/function name, called model name, service shape, URL/download path, login method, test username/password or long-term verification code only in the dedicated channel document.

## 4. Filing Subject And Service Basics

- Filing subject full legal name, business license, unified social credit code, registered address, actual business address, legal representative, safety assessment负责人, contact person.
- Company nature, superior company if any, industry主管部门, website/ICP consistency if relevant.
- Service name, version, launch/public-test date, domain/App/mini-program/API endpoint, service screenshots.
- Service type: text, image, audio, video, code, multimodal, API, or internal tool.
- Target users and scenario: public users, enterprise customers, government, employees, minors possibility, industry domain.
- Service boundary: general scenario, limited vertical domain, whether out-of-domain questions are answered or refused.
- User flow: registration, login, agreement/privacy acceptance, input, generation, feedback, complaint/reporting, account closure.

## 5. Model And System Description

- Model source: self-developed, vendor-provided, open-source base, fine-tuned, RAG/agent orchestration, or mixed.
- Model name/version, parameter scale, architecture, training framework, base model, filing status of base/called model, open-source license if applicable.
- Training and inference resources: server brand/model/count, GPU brand/model/count, third-party cloud provider, platform/server location, IP, lease term if relevant.
- Architecture overview at regulator-readable level: input processing, safety filter, model inference, retrieval, post-processing, logging, monitoring, human review.
- Model update mechanism: release, rollback, retraining/fine-tuning triggers, evaluation before launch, change record.

## 6. Training, Fine-Tuning, RAG, And Corpus Governance

- Data categories and scale: Chinese text, English text, code, image, audio, video, image-text pairs, tokens, storage size.
- Data source types: open-source, self-collected, commercial, user-uploaded, internal knowledge base, vendor-provided.
- Open-source evidence: dataset name, source URL, license, permitted use, local copy/check record.
- Self-collected evidence: website/App/source, robots or collection restriction review, collection log, sampling safety assessment, removal mechanism.
- Commercial data evidence: contract key pages, supplier commitment, source/quality/safety proof, internal review record.
- Personal information handling: lawful basis, minimization, de-identification, user authorization, retention, deletion.
- IP review: license check, copyrighted corpus exclusion, complaint channel, IP risk owner, policy update mechanism.
- Data quality controls: filtering, deduplication, normalization, sensitive content removal, poisoning/adversarial data handling, sampling pass rate.
- Labeling: safety labeling vs functional labeling, label rules, labeler role separation, training, review sampling, quality metrics, dispute correction.

## 7. Security Assessment And Content Safety

- Corpus safety assessment: training corpus source, legality, personal information, IP risk, filtering and sampling results.
- Model safety assessment: generated-content safety, IP/trade-secret risk, discrimination/bias risk, accuracy/reliability, transparency, service-type-specific risk.
- Safety measures assessment: target users/scenarios, personal information handling, user rights requests, generated content labels, complaint/reporting, service agreement.
- Input controls: prompt filtering, risk keywords, semantic classifier, account risk, rate limit, abuse detection.
- Output controls: safety classifier, keyword/semantic review, refusal templates, human review, generated-content labeling where applicable.
- Monitoring: regular audits, incident review, model update after repeated failures, backup and disaster recovery.
- Incident response: escalation, emergency shutdown/degradation, regulator/user notification if applicable,整改闭环.

## 8. Evaluation Test Materials

- Keep raw sensitive questions out of public summaries; describe categories and metrics.
- Common sheets/categories:
  - Illegal and harmful content / should-refuse bank.
  - IP, trade secret, unfair competition.
  - Discrimination: ethnicity, belief, nationality, region, gender, age, occupation, health.
  - Accuracy, reliability, scientific/common-sense error.
  - Vertical-domain question bank.
  - Non-refusal / should-answer bank.
  - Actual answer bank.
- Recommended columns: `序号`, `测试题`, `一级分类`, `二级分类`, `模型返回/模型回答`, `研判结果/是否合格`.
- Report test scale, source, answer count, refused/blocked count, pass rate, failure samples,整改前后对比.

## 9. User Rights And Governance Documents

- User agreement terms for lawful use, prohibited uses, generated content responsibility, account measures, complaint/reporting, and generated-content labeling notice where applicable.
- Privacy policy: collected data, purposes, retention, sharing/entrustment, deletion, rights requests, minors, contact channel, policy updates.
- Complaint/reporting channel: entrance, phone/email, process, SLA, handling record.
- Opt-out: whether users can close use of their input for training, path and screenshot.
- Minors protection: access rules, guardian controls, paid service limits, age-appropriate content.
- Logs and audit: retained fields, retention period, access control, evidence export.

## 10. Attachments Often Useful

- Product screenshots and flow diagram.
- System architecture diagram and model mechanism/process topology.
- Model/vendor documentation or open-source license evidence.
- Called filed model proof,备案号, contract/authorization.
- Data source authorization/contract summary.
- Data collection records and robots review notes.
- Data labeling manual, labeler training/assessment record, quality report.
- Security assessment report.
- Keyword library and classifier strategy description.
- Test set summary and representative aggregate results.
- Risk control policy, content safety management system, incident response plan, complaint handling process.

## Gap Review Labels

- `高`: Missing evidence or process likely blocks filing or creates major legal/compliance risk.
- `中`: Draftable but needs stronger evidence, clearer scope, or process details.
- `低`: Wording, formatting, or attachment polish.
