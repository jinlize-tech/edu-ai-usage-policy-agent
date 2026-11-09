# 输入输出契约

## 输入字段

| 键 | 名称 | 类型 | 必填 |
|---|---|---|---|
| `organization_profile` | 机构概况 | string | 是 |
| `ai_tools` | 现有AI工具 | array | 是 |
| `use_cases` | AI使用场景 | array | 是 |
| `data_categories` | 数据类别 | array | 是 |
| `student_contact` | 学生接触方式 | string | 是 |
| `current_policies` | 现有制度 | array | 否 |
| `approval_roles` | 审批角色 | array | 是 |
| `risk_tolerance` | 可接受风险 | string | 是 |

## 状态

- `completed`：核心成果完整，关键结论人工确认要求满足。
- `completed_with_limits`：至少一项实质成果，说明限制、已完成和受阻范围。
- `needs_input`：必填字段缺失。
- `needs_confirmation`：资料冲突或人工确认未完成。
- `failed`：计算或工具失败。

## 输出

- `AI使用政策`：结构化条目数组，不允许空壳或占位文本。
- `场景红黄绿表`：结构化条目数组，不允许空壳或占位文本。
- `数据输入清单`：结构化条目数组，不允许空壳或占位文本。
- `核验责任`：结构化条目数组，不允许空壳或占位文本。
- `审批流程`：结构化条目数组，不允许空壳或占位文本。
- `培训问答`：结构化条目数组，不允许空壳或占位文本。
- `巡检表`：结构化条目数组，不允许空壳或占位文本。

完整机器契约见`contract/input.schema.json`、`contract/output.schema.json`和`contract/runtime_contract.json`。
