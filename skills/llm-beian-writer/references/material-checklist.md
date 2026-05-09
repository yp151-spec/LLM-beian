# Material Checklist

This checklist is for drafting and gap review. Actual filing portals and local regulators may request different names, formats, or attachments.

## 1. Filing Subject And Service Basics

- 备案主体 full legal name, business license, unified social credit code, registered address, contact person.
- Service name, version, launch status, domain/App/mini-program/API endpoint, service screenshots.
- Service type: text, image, audio, video, code, multimodal, API, or internal tool.
- Target users and scenario: public users, enterprise customers, employees, minors possibility, industry domain.
- User flow: registration, login, input, generation, feedback, complaint/reporting, account closure.

## 2. Model And System Description

- Model source: self-developed, vendor-provided, open-source base, fine-tuned, RAG/agent orchestration, or mixed.
- Model name/version, deployment region, inference stack, model provider/vendor, open-source license if applicable.
- Architecture overview at regulator-readable level: input processing, safety filter, model inference, retrieval, post-processing, logging.
- Update mechanism: version release, rollback, evaluation before launch, change record.

## 3. Training, Fine-Tuning, RAG, And Corpus Governance

- Data categories, source list, collection method, lawful basis, authorization/contract evidence.
- Copyright/IP review and personal information handling basis.
- Data quality controls: filtering, deduplication, normalization, sensitive content removal, poisoning/adversarial data handling.
- Labeling rules, labeler training, review sampling, quality metrics, dispute correction.
- Knowledge base/RAG governance: document source, permission boundaries, update/removal, citation behavior, cache/logging.

## 4. Security Assessment And Content Safety

- Risk categories: illegal/harmful content, discrimination, privacy leakage, IP infringement, misinformation, minors, cyber abuse, domain-specific harms.
- Input controls: prompt filtering, rate limit, abuse detection, account risk scoring, blocked patterns.
- Output controls: safety classifier, keyword/semantic review, refusal templates, human review, generated-content labeling where applicable.
- Evaluation: test set design, red-team cases, pass/fail rules, sampling records, known limitations, remediation history.
- Incident response: monitoring, escalation, emergency shutdown/degradation, regulator/user notification if applicable.

## 5. User Rights And Governance Documents

- User agreement terms for lawful use, prohibited uses, generated content responsibility, account measures.
- Privacy policy: collected data, purposes, retention, sharing, deletion, rights requests, contact channel.
- Complaint/reporting channel: location, process, SLA, handling record.
- Minors protection: access rules, anti-addiction/overreliance controls if relevant.
- Logs and audit: retained fields, retention period, access control, evidence export.

## 6. Attachments Often Useful

- Product screenshots and flow diagram.
- System architecture diagram.
- Model/vendor documentation or open-source license evidence.
- Data source authorization/contract summary.
- Data labeling manual and quality report.
- Security assessment report.
- Test set summary and representative test results.
- Risk control policy, incident response plan, complaint handling process.

## Gap Review Labels

- `高`: Missing evidence or process likely blocks filing or creates major legal/compliance risk.
- `中`: Draftable but needs stronger evidence, clearer scope, or process details.
- `低`: Wording, formatting, or attachment polish.
