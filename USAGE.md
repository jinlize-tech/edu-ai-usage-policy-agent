# 使用说明

## 适用任务

教师用AI出题、家长服务人员用AI回复投诉，机构需要明确哪些可直接用、哪些必须双人核验。

## 1. 准备输入

机构业务与角色、现有AI工具、典型场景、数据类别、地区要求、教学原则、可接受风险、审批角色。使用前先脱敏姓名、联系方式和与任务无关的敏感信息。

安装包不包含`examples/typical_input.json`或`test-results/`。请根据`contract/input.schema.json`创建自己的`input.json`，字段名称、类型和必填要求以Schema为准。

## 2. 校验输入

```powershell
node scripts/validate_input.js input.json
```

如只需获得处理前状态和缺失项，可运行：

```powershell
node scripts/prepare_result.js input.json
```

## 3. 执行专业任务

按`SKILL.md`或Agent定义完成分析。输入缺失时返回`needs_input`；资料冲突或需人工确认时返回`needs_confirmation`；不得用空成果冒充`completed`。

## 4. 校验输出

将产品生成的最终JSON保存为`output.json`，然后运行：

```powershell
node scripts/validate_output.js output.json
```

校验只证明输出符合结构与完成状态契约，不替代真实模型运行、业务复核或平台验收。

## 5. 人工确认

负责人/教学/IT/法务复核AI允许场景、数据输入、人工核验、处罚和例外审批后，成果才可进入正式业务使用。

## 状态使用

- `completed`：核心成果完整且可复核。
- `completed_with_limits`：只完成可验证部分，并说明受限原因、已完成范围和受阻范围。
- `needs_input`：缺少关键输入。
- `needs_confirmation`：资料冲突或人工确认未完成。
- `failed`：工具或计算失败，提供恢复动作。
