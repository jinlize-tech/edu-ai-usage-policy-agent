# 教育机构AI使用政策制定

结合业务场景与平台规则制定AI使用政策、审批流程、人工核验、数据分级和违规处理。

## 适用用户

校长、教学负责人、HR、IT/数据负责人、教师代表

## 主要输出

- AI使用政策
- 场景红黄绿表
- 数据输入清单
- 核验责任
- 审批流程
- 培训问答
- 巡检表

## 安装

将Agent目录按平台要求导入，并保留`.codebuddy-plugin/plugin.json`、`agents/`、`skills/`与`avatars/`的相对结构。

本地验证：

```powershell
node scripts/validate_input.js examples/typical_input.json
node scripts/validate_output.js examples/typical_output.json
```

## 使用

1. 阅读`USAGE.md`。
2. 按`contract/input.schema.json`准备输入。
3. 调用产品或Agent完成专业处理。
4. 使用`scripts/validate_output.js`检查成果。
5. 高风险结论交由负责人/教学/IT/法务确认。

## 边界

- 不使用外部收费API。
- 不依赖其他产品完成核心任务。
- 不自动执行正式审批、退款、人员处罚或系统变更。
- 客户可见内容不包含公司品牌推广或内部研发资料。

## 状态

- 版本：`1.0.0`
- 本地契约与自动化测试：见`test-results/`
- 生成式模型运行：`MODEL_RUNTIME_NOT_VERIFIED`
- WorkBuddy安装、调用、审核、上架：`NOT_EXECUTED`
- 安装包：`dist/edu-ai-usage-policy-agent-v1.0.0.zip`

## 许可证

Apache-2.0。详见`LICENSE`。
