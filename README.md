# 毛发毒品检验智能体 · 交互演示

**Hair Drug Testing Agent · Interactive Demo**

配套研究：**基于大语言模型的毛发毒品检验智能体研发与验证**。

本网页以既有仿真执行轨迹为依据，展示毛发检验中前处理、仪器分析、数据处理、质量控制与结果复核的衔接，以及智能体在关键检查点的判断与反馈处理。页面默认中文，可通过语言按钮切换英文；在演示地址末尾添加 `?lang=en` 可直接打开英文版，`?lang=zh` 打开中文版。

### 演示场景

| 编号 | 场景 | 核心判断 |
| --- | --- | --- |
| P01 | 回执丢失：确认后重试 | 核验实际未执行后，再执行前处理 |
| P02 | 回执丢失：避免重复执行 | 核验实际已完成后，同步状态而不重复处理 |
| I01 | 积分疑点：重处理后通过 | 重新处理积分并保留版本与复核记录 |
| Q02 | 批次质控异常：暂停整批 | 根据批次质控异常暂停整批后续处理 |

这是可交互的 **source replay（源轨迹回放）**。动画根据已有执行记录组织，不在浏览器中实时调用模型或控制设备；重复的批内操作可合并展示，机械臂运动用于示意。页面中的样本、目标物、浓度与信号用于仿真演示。

---

## English

Companion demo for **Development and Validation of a Large Language Model-Based Agent for Drug Testing in Hair**.

This interactive page presents coordination across sample preparation, instrumental analysis, data processing, quality control, and result review. It replays existing simulation trajectories to illustrate decisions at key checkpoints and responses to execution feedback.

Chinese is the default language. Use the language button or append `?lang=en` to the demo URL for English (`?lang=zh` for Chinese).

| ID | Scenario | Decision illustrated |
| --- | --- | --- |
| P01 | Missing acknowledgement: verify, then retry | Confirm that preparation did not occur before retrying |
| P02 | Missing acknowledgement: prevent duplicate execution | Confirm completion and synchronize state without repeating preparation |
| I01 | Integration concern: reprocess and review | Reprocess integration and retain version and review records |
| Q02 | Batch quality-control failure: hold the batch | Stop subsequent processing for the entire affected batch |

The demo is a **source replay**, not live model inference or device control. Animation follows recorded simulation events, with some repeated batch operations grouped for presentation. Robotic motion is illustrative; samples, analytes, concentrations, and signals are synthetic demonstration data.
