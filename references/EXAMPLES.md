# 教育机构AI使用政策制定示例

## 典型场景

教师用AI出题、家长服务人员用AI回复投诉，机构需要明确哪些可直接用、哪些必须双人核验。

## 具体示例

Agent 生成分场景政策和审批表，并明确客户数据、学生数据和未公开题库不得擅自输入外部工具。

## 脱敏输入示例

```json
{
  "contract_version": "1.2.0",
  "data_status": "confirmed",
  "contains_sensitive_data": false,
  "requested_output_language": "zh-CN",
  "organization_profile": "机构概况已核对（脱敏示例）",
  "ai_tools": [
    {}
  ],
  "use_cases": [
    {}
  ],
  "data_categories": [
    {}
  ],
  "student_contact": "学生接触方式已核对（脱敏示例）",
  "current_policies": [
    {}
  ],
  "approval_roles": [
    {}
  ],
  "risk_tolerance": "可接受风险已核对（脱敏示例）",
  "resume_mode": "new"
}
```

## 预期处理

1. 运行输入契约校验。
2. 逐项核对输入来源、版本和口径。
3. 按`references/PROFESSIONAL_PLAYBOOK.md`完成专业分析。
4. 输出AI使用政策、场景红黄绿表、审批流程等核心成果。
5. 由负责人/教学/IT/法务确认AI允许场景、数据输入、人工核验、处罚和例外审批后才可作为正式业务结论。

## 不应出现的输出

- 虚构政策、价格、人员、课程或客户事实。
- 以“暂无”“待完善”等占位文本冒充完成。
- 无依据的确定性判断或伪造人工签批。
