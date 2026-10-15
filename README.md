# domn-character-poster

![domn-character-poster 封面](assets/readme/hero.webp)

> 原创角色宣传物料：参考图 → 主视觉海报 / 人物设定图。

## 是什么

原创角色宣传物料：参考图 → 主视觉海报 / 人物设定图。本仓库是一个 Agent 技能（SKILL.md 为唯一权威定义），把上面的方法论沉淀为可被对话触发的可执行流程。

## 怎么做（工作流）

<p align="center">
  <img src="./assets/readme/workflow.svg" width="100%" alt="domn-character-poster 工作流：角色锁定 → 成像锁定 → 视觉锚点 → 定演出 → 成稿。七项视觉锚点锁长相，防海报风格污染">
</p>

1. **角色锁定**
2. **成像锁定**
3. **视觉锚点**
4. **定演出**
5. **成稿**

## 怎么用

将本仓库放入支持 `SKILL.md` 的 Agent 技能目录：

- **WorkBuddy**：`~/.workbuddy/skills/domn-character-poster/`
- **Codex / 其他**：对应 skills 目录

然后在对话中触发，例如：

```
用 domn-character-poster 帮我处理一段需求。
```

## 依赖

纯提示词方法论 + references/ 弹药库；出图依赖图像生成模型.

## 仓库结构

```
domn-character-poster/
├── SKILL.md                 # 技能定义（唯一权威）
├── references/              # 方法论弹药库
├── assets/                  # 模板 / 占位素材
└── assets/readme/           # 本 README 的视觉资产（hero.webp / workflow.svg）
```

## 许可

本仓库内容以 `SKILL.md` 为唯一权威定义。如附带 `LICENSE` 文件，以其为准。

---

*README 由 `beautify-github-readme` 生成 · 封面图来自作者作品集，强调色由封面图采样派生。*
