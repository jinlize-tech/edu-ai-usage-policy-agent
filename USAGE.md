# 使用说明

## 适用任务

教师用AI出题、家长服务人员用AI回复投诉，机构需要明确哪些可直接用、哪些必须双人核验。

## 准备输入

机构业务与角色、现有AI工具、典型场景、数据类别、地区要求、教学原则、可接受风险、审批角色。使用前先脱敏姓名、联系方式和与任务无关的敏感信息。

## 操作步骤

1. 盘点AI场景
2. 分级风险
3. 制定用途与数据规则
4. 设计人工核验和审批
5. 培训与例外管理
6. 试点和复核

## 校验命令

```powershell
node scripts/validate_input.js examples/typical_input.json
node scripts/validate_output.js examples/typical_output.json
```

## 状态使用

- `completed`：核心成果完整。
- `completed_with_limits`：只完成可验证部分，并说明受阻范围。
- `needs_input`：缺少关键输入。
- `needs_confirmation`：资料冲突或需人工确认。
- `failed`：工具或计算失败，提供恢复动作。

## 人工确认

负责人/教学/IT/法务复核AI允许场景、数据输入、人工核验、处罚和例外审批后，成果才可进入正式业务使用。
