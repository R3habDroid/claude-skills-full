# Claude Skills — Full

Anthropic 官方 skills 的「最全版」整理。上游 [`anthropics/skills`](https://github.com/anthropics/skills) 在 2026 年对 document-processing 系列 skill 做了两次精简,砍掉了 `html2pptx`、`ooxml` 深度文档、`docx-js`、`inventory`/`rearrange`/`replace`、`recalc.py` 等能力。本仓库把这些内容恢复回来。

A "fullest" consolidation of the official Anthropic skills, restoring the document-processing capabilities (html2pptx, ooxml, docx-js, inventory/rearrange/replace, recalc.py) that were removed from `anthropics/skills` during 2026.

## 与官方仓库的差异 / What was restored

| Skill | 恢复的内容 / Restored |
|-------|----------------------|
| **pptx** | `html2pptx.md` + `html2pptx.js`(HTML→PPT)、`ooxml.md`、`inventory.py`、`rearrange.py`、`replace.py`、ooxml 工具链 |
| **docx** | `docx-js.md`、`ooxml.md`、`document.py`、`utilities.py`、ooxml 工具链 |
| **xlsx** | `recalc.py`(公式重算) |
| **pdf** | `check_bounding_boxes_test.py` |
| **skill-creator** | `output-patterns.md`、`workflows.md`、`init_skill.py` |

其余 skill 与上游最新版保持一致(含 `claude-api`、`academy-guide`、`discernment-nudge` 等 2026 年新增)。

## 目录结构 / Layout

```
skills/
  algorithmic-art/  brand-guidelines/  canvas-design/  claude-api/
  discernment-nudge/  doc-coauthoring/  docx/  frontend-design/
  internal-comms/  mcp-builder/  pdf/  pptx/  skill-creator/
  slack-gif-creator/  theme-factory/  web-artifacts-builder/
  webapp-testing/  xlsx/  academy-guide/
```

## 许可 / License

各 skill 保留其原始 `LICENSE.txt`(Anthropic 专有许可)。本仓库仅做整理与还原,不改变任何许可条款。Each skill keeps its original `LICENSE.txt` (Anthropic proprietary license).

## 安装 / Install

将 `skills/` 下的内容复制到你的 Claude 技能目录(如 `~/.claude/skills/`)即可:

```bash
cp -r skills/* ~/.claude/skills/
```
