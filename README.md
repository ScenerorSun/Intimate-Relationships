# Intimate-Relationships — 亲密关系 Skill 蒸馏包

> 把罗兰·米勒《亲密关系》（Intimate Relationships, 6th Edition）蒸馏成一组可被 AI Agent 调用的关系科学 skills。

## 这是什么

一本 500 页的教材，拆成 8 个原子化的、带触发条件的、可执行的 AI skills。每个 skill 都是一个 `SKILL.md`，包含：

- **R** — 原文引用（标注出处）
- **I** — 方法论骨架（用自己的话重写）
- **A1** — 书中的应用案例
- **A2** — 触发场景与语言信号（何时该激活）
- **E** — 可执行步骤（含完成标准）
- **B** — 边界与失败模式（何时不该用）

蒸馏流水线：cangjie-skill（RIA-TV++：Adler 分析 → 5 提取器并行 → 三重验证 → RIA++ 构造 → Zettelkasten 链接 → 压力测试 → 交付）。

## Skill 列表

| skill | 一句话定位 | 触发关键词 |
|-------|-----------|-----------|
| `relationship-diagnosis` | 关系六要素体检，定位薄弱项 | 关系有问题 / 没那么亲密 |
| `attachment-mapper` | 依恋二维模型，理解自己的关系模式 | 太依赖 / 太冷淡 / TA 不回消息 |
| `attraction-principles` | 拆解吸引力来源与质地 | 为什么被 TA 吸引 / 合不合适 |
| `perception-debiaser` | 修正关系中的认知偏差与误读 | TA 就是故意的 / 总觉得 TA 会背叛 |
| `conflict-deescalation` | 冲突降级：四骑士识别 + 5:1 修复 | 又吵架 / 冷战 / 怎么和好 |
| `communication-upgrader` | 日常沟通升级：表露/表述/倾听/资本化 | 聊天越来越干 / 怎么表达需求 |
| `commitment-assessor` | 投入模型评估该不该继续 | 该不该分手 / 只是习惯 |
| `breakup-recovery-guide` | 分手后阶段化恢复 | 走不出来 / 删不删 TA |

## 目录结构

```
.
├── BOOK_OVERVIEW.md        # 整书理解（Adler 四步）
├── verified.md             # 三重验证通过的单元 + 判定理由
├── INDEX.md                # skill 地图 + 引用图
├── GLOSSARY.md             # 共享术语词典
├── DIGEST.md               # 精华长文（不读全书也够用）
├── PIPELINE_STATE.md       # 蒸馏流水线状态
├── candidates/             # 原始候选池（审计用）
├── rejected/               # 被淘汰单元 + 原因
└── <skill-slug>/
    ├── SKILL.md            # skill 本体（可被 agent 加载）
    ├── test-prompts.json   # 触发测试（含诱饵题）
    └── description.md      # 知乎文体简介
```

## 如何使用

三种方式：

1. **直接读 `DIGEST.md`** — 只想了解核心方法论，5 分钟读完精华。
2. **把某个 `<skill>/SKILL.md` 安装到你的 Agent skills 目录**（如 `~/.workbuddy/skills/` 或项目 `.claude/skills/`），Agent 就能在你"关系出问题了""又吵架了""走不出来"等场景自动调用对应方法论。
3. **用 `test-prompts.json` 验证触发** — 每个 skill 附测试用例，含应调用/不应调用（诱饵）场景。

## 使用路径建议

- 关系刚出问题：`relationship-diagnosis`（体检）→ 定位薄弱项
- 反复冲突：`perception-debiaser`（先去偏）→ `conflict-deescalation`（降级）→ `communication-upgrader`（重建）
- 自我认知：`attachment-mapper`（理解模式）→ 针对调整
- 纠结去留：`commitment-assessor`（三变量）→ 留下经营 / 离开恢复

## 关键概念速查

- **亲密关系六要素**：了解 / 关心 / 相互依赖 / 相互一致 / 信任 / 承诺
- **依恋二维模型**：回避亲密 × 忧虑被弃 → 安全 / 痴迷 / 疏离 / 恐惧
- **投入模型**：承诺 = 满意度 + 替代吸引 + 投入
- **末日四骑士**：批评 → 蔑视 → 防卫 → 筑墙（预测离婚准确率 94%）

## 版权说明

- 原书版权归罗兰·米勒（Rowland S. Miller）所有。
- 本仓库的 SKILL.md 为方法论蒸馏产物（引用片段 ≤150 字，用于学术讨论）。
- 蒸馏工具：kangarooking/cangjie-skill（AGPL-3.0）。本仓库内容为独立创作，非衍生代码。

## 蒸馏信息

- 蒸馏日期：2026-08-04
- 蒸馏方式：cangjie-skill RIA-TV++ 流水线
- 源文本：Z-Library 电子版全文 → Markdown

---

*由既明博士工作流自动生成。*
