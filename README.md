[中文](./README.md) · [English](./README.en.md)

# BluffKing Blog

> 一个几乎完全由 AI 编码 agent 构建的扑克 app，背后的工程「构建笔记」。

本仓库（`CisaSettle/bluffking-blog`）是 BluffKing 双语（中文 / English）工程「构建笔记」博客的**公开源码仓库**：一组自包含的双语 HTML 文章，零构建、无框架。

[BluffKing](https://bluffking.ai) 是一款浏览器端的无限注德州扑克（No-Limit Texas Hold'em）app，几乎完全是**用 AI 编码 agent 构建**的（Claude Code + OpenAI Codex）。这个博客记录那段构建过程：agent 编排、Rust、确定性扑克逻辑。我们把笔记开源，是因为「让一支 agent 团队真正干活」这件事本身值得被写下来——也值得被复用。

## 线上博客

正式（canonical）的线上博客在营销主站；本仓库的内容会被镜像到那里渲染：

- 中文：<https://bluffking.ai/zh/blog/>
- English：<https://bluffking.ai/en/blog/>
- 首篇文章：<https://bluffking.ai/zh/blog/why-worktrees/> · <https://bluffking.ai/en/blog/why-worktrees/>

本仓库同时通过 GitHub Pages 镜像提供访问：<https://cisasettle.github.io/bluffking-blog/>。但该镜像的 `rel=canonical` 指向 `bluffking.ai/zh/blog/`——也就是说它**让位于**正式站点，并非一个与之竞争的地址。

## 仓库结构

每篇文章都是一个**自包含的 HTML 文件**：无构建步骤、无框架、双语内置。

| 文件 | 说明 |
| --- | --- |
| `index.html` | 静态落地页，列出全部文章；带 中文/English 切换（用 `localStorage` 持久化，默认中文）。 |
| `<slug>.html` | 每篇文章一个自包含 HTML 文件（如 `why-worktrees.html`）。两种语言均内置，页内 中文/English 切换，默认中文，绿色品牌配色。 |
| `.nojekyll` | 让 GitHub Pages 原样提供文件，不经 Jekyll 处理。 |
| `README.md` / `README.en.md` | 即本双语 README。 |

### 一篇文章的结构

- **自包含的双语 HTML**：中文与英文都写在同一个文件里。
- **页内切换**：通过 中文/English 切换在两种语言间切换，**默认中文**。
- **永不行内混排**：同一时间只显示一种语言，绝不把两种语言并排混在一起。
- **零依赖**：无外部依赖、无构建、无框架——直接用浏览器打开即可。

## 已有文章

| 日期 | Slug | 标题 | 标签 |
| --- | --- | --- | --- |
| 2026-06-20 | `why-worktrees` | 为什么每个 AI 编码 agent 都该有自己的 git worktree | git worktree · Claude Code · Codex · agent 编排 |

## 新增文章

1. 复制一个已有的 `<slug>.html` 作为模板。
2. 在文件内同时写好**中文和英文**，放在切换之后（默认中文，**永不行内混排**）。
3. 在 `index.html` 里加一张对应的文章卡片。
4. 提交。

同一篇文章还需镜像进营销主站（`website/content/posts/<slug>/{zh,en}.html`）——那才是驱动正式 `bluffking.ai` 博客的源头。

## 关于 BluffKing

BluffKing 是一款浏览器端的无限注德州扑克，几乎完全由 AI 编码 agent 构建（Claude Code + OpenAI Codex）。本博客记录这一构建过程：agent 编排、Rust、以及确定性扑克。

---

主站 [bluffking.ai](https://bluffking.ai) · X / Twitter [@BluffKingAI](https://x.com/BluffKingAI)
