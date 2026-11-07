# G5/G9 产品修改记录

- 产品编号：$(@{number=62; product_id=JLZ-EDU-SK-050; chinese_name=家长投诉分类; english_name=Complaint Classifier; repository_name=edu-complaint-classifier; repository_url=https://github.com/jinlize-tech/edu-complaint-classifier; product_type=Skill; category_code=05; category=05 家校服务中心; description=投诉问题分类。; target_users=System.Object[]; core_input=投诉原话、发生环节、涉及人员、时间、诉求、证据状态和敏感信息; main_output=问题分类、严重度、事实与推断分离、升级路径、需核实项和记录摘要; product_risk=对事实未核先定性或泄露个人信息; dedup_label=无明显重复; dedup_note=与投诉回复区别：本产品只分类和评估，不生成对外答复。; development_status=Planned / 待研发; license=Apache-2.0; spec_version=1.0.0; workbuddy_status=PLANNED_FOR_WORKBUDDY}.product_id)
- 产品名称：家长投诉分类
- 基线：EDUCATION_BASELINE_V1.0.0
- 基线提交：$BaselineCommit
- 原版本：1.0.0
- 新版本：1.0.1

## 本次修改

1. 强化产品专属执行流程、输入核对和输出验收规则。
2. 新增 scripts/validate_input.js，实际检查必填字段、冲突、未确认数据和敏感信息。
3. 新增正常、缺失、冲突、敏感信息和非法JSON场景输入。
4. 测试升级为 T1–T7 分层并保存逐项检查结果。
5. 安装包加入 Apache-2.0 LICENSE 和 THIRD_PARTY_NOTICES.md。
6. 安装包升级为 1.0.1，加入许可证、第三方声明和输入校验脚本，保留 1.0.0 ZIP。
7. 按本产品冻结规格补充专属处理规则、输入到成果的核对矩阵和去重边界。

## 产品专属增强

- 核心任务：投诉问题分类。
- 主要风险：对事实未核先定性或泄露个人信息
- 去重边界：与投诉回复区别：本产品只分类和评估，不生成对外答复。

- 先确认事实、涉及对象、沟通目的、渠道、时间要求和必须披露的信息。
- 给家长或学生的结论必须区分事实、观察、建议和待核实内容。
- 只披露与该家庭直接相关且确有必要的学生信息，避免交叉泄露。
- 投诉、退款、安全和健康事项设置人工升级条件，不替代正式处置。

## 运行边界

- 本地模型行为：NOT_RUNTIME_VERIFIED
- WorkBuddy平台验证：WORKBUDDY_VALIDATION_NOT_IN_SCOPE
- 本轮不执行上传、安装、审核或正式发布。
