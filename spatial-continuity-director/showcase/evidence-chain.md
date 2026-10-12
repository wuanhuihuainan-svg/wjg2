# Skill → 成片证据链

| 环节 | 证据 | 可核验点 |
|---|---|---|
| 资产绑定 | `spatial_plan.json.asset_registry` | 场景、两个人物与道具各有唯一职责；场景图中的无关人物已登记并通过空场景底图降级 |
| 空间 | `anchors` 与 `blocking_map` | 三个固定锚点、动作因果、轴线和时空碰撞通过 |
| 分段 | `segments` | 三段合计 30 秒；每段有风险等级、主动作、接收状态、接棒和回退剪点 |
| 首帧 | 每段 `start_keyframe` | 单一主驱动；人物、空间、道具、构图 QC 均通过 |
| 引用 | `reference_inputs` / `attached_references` | 每张图职责清楚，超出平台上限的资产进入 `unattached_assets` |
| 音频 | `audio_ledger` | 两句对白各出现一次且有片段归属 |
| 生成门 | `approvals` | 资产/首帧与模型/提示词两级确认完成 |
| 生成后 | `post_generation_qc` | 首、中、尾抽帧核对身份、锚点、道具、动作因果和接棒 |

不能用提示词文件本身证明生成成功；只有画布节点、输出视频和真实抽帧 QC 才能证明结果。
