# Filing Boundary: 大模型备案 vs 算法备案

Use this reference whenever a request mixes `大模型备案`, `生成式人工智能服务备案`, `算法备案`, `深度合成`, or `生成合成内容标识`.

## Core Distinction

| Dimension | 大模型备案 / 生成式AI服务备案 | 算法备案 |
| --- | --- | --- |
| Primary object | Generative AI service, large language model, filed/called model, product or function that provides generation | Internet information service algorithm, such as generation/synthesis, recommendation, ranking, filtering, dispatch/decision |
| Typical route | Full online filing, registration for calling a filed model, new product/new function filing | Algorithm filing in stages: subject information, algorithm/product information, self-assessment, public mechanism content |
| Main concern | Model/service safety, corpus safety, model output safety, service agreement, privacy, test questions, keyword library, test channel/API | Algorithm mechanism, data/model/strategy, user rights, algorithm security responsibility, public explanation, product function and access path |
| Typical documents | 上线备案表, 安全评估报告, 模型/产品服务协议, 隐私政策, 语料标注规则, 拦截关键词列表, 评估测试题, 测试账号/API, 其他佐证 | 算法备案承诺书, 落实算法安全主体责任基本情况, 算法安全自评估报告, 拟公示算法机制机理内容, 算法基础信息/详细属性/产品功能信息 |
| Evidence shape | Corpus source, model filing proof, data contracts, sampling results, safety tests, service screenshots, generated-content controls | Algorithm flow, algorithm type, algorithm name, input/output modalities, intervention strategy, result labels, user rights screenshots, product path |
| Common terms | 大语言模型, 生成式人工智能服务, 调用已备案大模型, 语料安全, 模型安全, 安全措施 | 生成合成类, 个性化推送类, 排序精选类, 检索过滤类, 调度决策类, 拟公示算法机制机理内容 |

## When Both May Be Needed

A public-facing AI product can require both tracks when it:

- Provides generative AI service to the public and therefore needs large-model/generative AI service filing.
- Uses an internet information service algorithm with public opinion properties or social mobilization capacity, or falls into algorithm filing categories such as generation/synthesis.
- Provides deep synthesis or generated/synthetic content where labeling, implicit mark, or public notice duties apply.

If both are needed, keep separate workstreams and map shared facts carefully:

- Model/service facts can feed both tracks, but do not copy document titles or conclusions across tracks.
- The model safety assessment can inform algorithm self-assessment, but the algorithm self-assessment must still describe algorithm flow, data, model, intervention strategy, result labels, user rights, and product path.
- The generated-content labeling section may be relevant to both, but cite it as a labeling/deep synthesis requirement, not as proof that model filing is complete.

## Algorithm Filing Deliverables To Keep Separate

Do not put these into a large-model filing package unless the regulator explicitly asks for them as a separate algorithm attachment:

- `互联网信息服务算法备案承诺书`
- `落实算法安全主体责任基本情况`
- `算法安全责任人工作证明`
- `互联网信息服务算法安全自评估报告`
- `拟公示算法机制机理内容`
- Algorithm portal fields such as algorithm type, role, application field, algorithm performance, hardware requirement, algorithm calculation method, product DAU/MAU, and product access path.

## Large-Model Filing Deliverables To Keep Separate

Do not replace these with algorithm filing materials:

- `生成式人工智能（大语言模型）上线备案表` or `登记备案表`
- `安全评估报告` covering corpus safety, model safety, safety measures, and overall conclusion
- `模型服务协议` / `产品服务协议`
- `隐私保护政策`
- `语料标注规则` or `内容安全管理制度` depending on route
- `拦截关键词列表`
- `评估测试题`
- `测试账号/API接口` documents
- `调用已备案模型情况说明及相关证明材料`

## Common Confusions

- `算法机理` in a large-model information collection form may mean model mechanism or technical route. It does not automatically mean the task is algorithm备案.
- A generated text model can appear in an algorithm self-assessment as a `生成合成类算法`; that does not replace the generative AI service filing package.
- `深度合成算法备案` and `人工智能生成合成内容标识` are related to generation/synthesis governance, but they are not the same as the large-model online filing form.
- A service agreement/privacy policy may support both tracks, but each track may ask for different screenshots and user-rights evidence.

## Practical Triage Questions

Ask these before drafting:

1. Is the deliverable being submitted to a large-model/generative AI service filing path, an algorithm filing path, or both?
2. Is the service public-facing or only internal?
3. Is the model self-developed, fine-tuned from an open-source base, or calling a model that already has a filing number?
4. Does the product include recommendation/ranking/filtering/dispatch or generation/synthesis algorithms beyond the model itself?
5. Does the product generate text, image, audio, video, virtual scenes, or other generated/synthetic content that needs explicit or implicit labeling?
