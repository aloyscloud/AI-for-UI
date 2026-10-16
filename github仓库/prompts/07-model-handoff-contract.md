# 多模型交接契约

每个模型只负责指定岗位，并输出以下结构。若入口不支持 JSON 输出，则使用完全相同字段的 Markdown。

```json
{
  "task_id": "项目内唯一任务编号",
  "role": "intake|explore|define|build|review|qa",
  "status": "complete|blocked|needs_human|failed",
  "inputs_used": ["实际读取的文件或证据"],
  "outputs_created": ["实际创建的文件"],
  "decisions": [{"decision": "决定", "reason": "理由"}],
  "evidence": [{"type": "screenshot|test|diff|log|manual_check", "path": "项目相对路径", "result": "观察结果"}],
  "assumptions": [],
  "open_questions": [],
  "risks": [],
  "next_action": "唯一、明确的下一步"
}
```

规则：不得虚构路径、截图、测试结果或工具能力。`complete` 只表示本岗位产物完成，不表示整个产品已验收。设计方向选择、事实确认和发布决定需要人类处理。下游模型必须读取文件证据，而不只依赖聊天摘要。若上游产物缺失或矛盾，先报告，不要静默猜测。
