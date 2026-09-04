# 抖音「云端避风港」创作手册

**Douyin Dream Shelter Style** · 灾难开场 / 第一人称 POV / 物品变身 / 巨型庇护所 / 室内体验 / 品牌软植入

本项目收录 `douyin-dream-shelter-style` 的全部原始内容，便于在 GitHub 中按章节阅读、查找规则、复用创作流程。原始 skill 以英文为主；中文首页、阅读指南和单集简报帮助理解与使用，完整规则请以原文为准。

**从这里开始：** [中文阅读指南](docs/reading-guide.md) · [完整 Skill](SKILL.md) · [案例与失败模式](references/case-library-and-failure-modes.md) · [单集简报模板](docs/episode-brief.md)

## 这套内容解决什么问题

把一集庇护所视频组织成一条可以看懂、可以跟随、具有情绪释放的连续体验：

> 正在工作的角色 → 近在眼前的威胁 → 灾难真正影响身体或路线 → 操作随身物件 → 专属材质遮满画面 → 巨型庇护所显现 → 合理进入 → 三段室内体验 → 在安全与温暖中结束。

它既能用于完整创意和客户大纲，也能用于一张首帧、一个 GPT Image 提示词、一处局部改图、一段视频衔接或一个品牌合作场景。按当前交付物选择规则，不必每次输出整集。

## 按问题阅读

| 你正在做什么 | 应读文件 | 主要内容 |
| --- | --- | --- |
| 初次了解账号风格、规划整集 | [SKILL.md](SKILL.md) | 创作语法、交付类型、整体流程、最终检查 |
| 设计灾难钩子、第一视角动作、物品变身 | [POV、灾难与变身](references/pov-disaster-transformation.md) | 最后安全一秒、双高潮、物理因果、遮挡、落地与入内 |
| 写 GPT Image 提示词、封面、白底资产、改图指令 | [图片提示词规范](references/gpt-image-prompt-contract.md) | 单段英文 Prompt、参考图角色、比例、人体、文字、局部锁定 |
| 规划三个空间、加强温暖和安全感 | [室内与图像编辑](references/interiors-and-image-edits.md) | 连续动线、尺度、配色、实际光源、夜景、局部修改 |
| 做品牌合作、产品体验、服务型庇护所 | [品牌融入](references/brand-integration.md) | 使用动机、空间化表达、虚拟服务角色、产品保真、柔和结尾 |
| 找已有思路、排查生成问题 | [案例库与失败模式](references/case-library-and-failure-modes.md) | 已有案例、局部验证经验、常见错误和修复方向 |
| 查看 skill 的显示名称与调用配置 | [agents/openai.yaml](agents/openai.yaml) | 显示信息、默认调用提示、隐式调用设置 |

## 推荐阅读顺序

1. 阅读 [中文阅读指南](docs/reading-guide.md)，理解叙事骨架与关键约束。
2. 阅读 [SKILL.md](SKILL.md)，获得完整的主规则。
3. 按任务进入上表中的专题参考。
4. 用 [单集简报模板](docs/episode-brief.md) 组织本次需求。
5. 对照 [案例库](references/case-library-and-failure-modes.md) 和主文件中的最终检查，修正具体问题。

## 作为项目交给 AI 阅读

把仓库提供给能够访问它的 AI 工具后，可以使用下面这段指令，再补充本次需求：

```text
请把这个仓库作为我的「云端避风港 / 庇护所」创作规范。
先阅读 README.md 和 SKILL.md，再根据本次任务阅读 references/ 中对应的完整文件。
docs/ 是中文导读与工作模板；如与原始文件存在差异，以 SKILL.md 和 references/ 为准。

先判断我需要的是创意、大纲、图片提示词、改图、视频衔接、室内方案还是品牌方案。
保持灾难因果、真实 POV、物品来源与操作、遮挡后揭示、合理进入、连续室内动线。
引用已有案例时，区分已验证的局部机制和仍未解决的问题。

本次需求：
[在这里填写主题、职业、灾难、物件、交付物和必须保留的细节]
```

如果只提供了部分文件，应明确已读范围；不要把尚未读取的参考文件当作已掌握内容。

## 目录结构

```text
douyin-dream-shelter-style/
├── README.md                              # 中文项目入口
├── SKILL.md                               # 原始主文件
├── SOURCE-MANIFEST.json                    # 原始 7 个文件的大小与 SHA-256
├── agents/
│   └── openai.yaml                         # 原始 skill 配置
├── references/
│   ├── pov-disaster-transformation.md      # POV、灾难、变身与入内
│   ├── gpt-image-prompt-contract.md        # 图片提示词与改图规范
│   ├── interiors-and-image-edits.md        # 室内、光照与局部编辑
│   ├── brand-integration.md                # 品牌与服务体验
│   └── case-library-and-failure-modes.md   # 案例、失败模式与修复
└── docs/
    ├── reading-guide.md                   # 中文内容导读
    └── episode-brief.md                   # 单集工作模板
```

## 内容来源与维护

- `SKILL.md`、`references/` 和 `agents/openai.yaml` 完整保留原始目录中的全部 7 个文件，未改写正文。
- [SOURCE-MANIFEST.json](SOURCE-MANIFEST.json) 记录导出时间、原始文件路径、字节数和 SHA-256，可用于检查快照完整性。
- `README.md` 与 `docs/` 是为项目阅读新增的中文说明和模板，不替代原始规则。
- 这是一次完整快照；本机 skill 后续更新时，需要同步文件并更新清单。
- 本项目收录的是这一份 skill。文中提及的其他提示词 skill 和外部参考素材没有随之复制。
