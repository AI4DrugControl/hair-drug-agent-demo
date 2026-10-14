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

### 打开与发布

- 本地预览：打开 `index.html`。
- GitHub Pages：新建独立公开仓库 `hair-drug-agent-demo`，将解压后的网页文件放到 `main` 分支根目录。在 **Settings → Pages → Deploy from a branch** 中选择 **main / (root)** 并保存。
- 无需 npm、模型权重、API 密钥或后端服务。
- 已有个人主页可继续保留。本项目使用独立仓库，不修改个人主页仓库，也无需新增 `CNAME`。正式演示网址以 GitHub Pages 的 **Visit site** 为准。

论文中的在线演示链接应在部署成功后填写，具体建议见压缩包附带的《论文链接说明》。

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

Open `index.html` locally, or publish the extracted files from the `main` branch root of a separate public repository named `hair-drug-agent-demo` using GitHub Pages. No npm installation, model weights, API key, or backend is required. A separate project site can coexist with an existing personal homepage. Use the final **Visit site** address shown in Pages settings when adding the demo link to the manuscript.

### GitHub documentation

- [GitHub Pages site types](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages)
- [Publishing from a branch](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
- [Custom domains across multiple repositories](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages)
