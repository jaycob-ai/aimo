# AIMO

> 每天说一句「AIMO」，把当天的 AI 进展整理成一份能长期存档的简报。

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Codex Skill](https://img.shields.io/badge/Codex-Skill-10a37f.svg)](aimo/SKILL.md)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

AIMO 是一个 Codex 技能（Skill）。它把「每天固定收集 AI 信息」压缩成一句话：输入 `AIMO`，它去公开信息源检索前一个自然日的 AI 动态，核对来源与日期，先给你一份候选清单；你说「全部加入」，它才写入本地 Markdown。

只写本地文件，不需要数据库，不需要服务器，不上传你的数据。

## 特性

- **先看后写**：默认只展示、不动文件，确认后才落盘
- **五个维度**：行业新闻、人物观点、开源项目、实用工具、论文
- **来源可追溯**：每条都附原始链接与日期
- **公司维度归档**：新闻自动关联公司/机构，日积月累形成可检索的数据库
- **纯本地**：不部署、不依赖云端、不碰你的其他文件

## 安装

需要先有 Codex（桌面版即可）和可用的网络。

### 方式一：让 Codex 自己装（推荐）

在 Codex 里发这一句话：

```
安装这个技能：https://github.com/jaycob-ai/aimo/tree/main/aimo
```

装完新开一个对话，输入 `AIMO` 即可。

### 方式二：手动放文件

1. 打开 skills 目录
   - macOS：访达按 `Cmd + Shift + G`，粘贴 `~/.codex/skills`
   - Windows：资源管理器地址栏粘贴 `%USERPROFILE%\.codex\skills`
2. 新建文件夹 `aimo`，把 [`aimo/SKILL.md`](aimo/SKILL.md) 放进去
3. 确认路径是 `~/.codex/skills/aimo/SKILL.md`，文件名必须是大写的 `SKILL.md`
4. 重开 Codex，输入 `AIMO`

## 使用

1. 用 Codex 打开一个用来放资料的文件夹
2. 输入 `AIMO`，等它给出候选清单
3. 回复编号挑选，或回复「全部加入」

| 口令 | 作用 |
| --- | --- |
| `AIMO` | 只检索、核验并展示候选，不写入 |
| `全部加入` | 把当前候选写入本地数据文件 |

## 产出文件

| 文件 | 内容 |
| --- | --- |
| `AI行业进展.md` | 公司/机构数据库与行业进展 |
| `每日热点.md` | 每天的新闻、论文、工具与人物观点 |

两个文件都创建在你打开的项目目录里，是纯 Markdown，可以随时用任何编辑器查看和修改。

## 数据来源

AIMO 优先引用一手来源，媒体只用于发现线索。默认覆盖：

- 行业新闻：AI HOT、量子位、36kr、雷锋网、TechCrunch、The Verge 等
- 人物观点：Karpathy、Sam Altman、黄仁勋、李飞飞、梁文锋等的官方账号与原始访谈
- 开源项目：GitHub Trending/Search、Hugging Face、各机构官方仓库
- 论文：arXiv、OpenReview、Hugging Face Daily Papers
- 工具与应用：编程 Agent、办公 Agent、研究工具、设计与效率工具

名单与监控范围都写在 [`aimo/SKILL.md`](aimo/SKILL.md) 里，可以直接改成你关心的方向。

## 常见问题

**说 AIMO 没反应？**

检查 `~/.codex/skills/aimo/SKILL.md` 是否存在，文件夹名和文件名都要对，然后重开 Codex。

**说完没生成文件，是坏了吗？**

没坏。只展示、不写入是设计如此，你确认之后才会落盘。

**需要联网吗？**

需要。它要访问公开信息源检索并核验当天内容。

**会改我的其他文件吗？**

不会。它只创建和更新上面那两个 Markdown 文件。

**可以改成自己的监控名单吗？**

可以。直接编辑 [`aimo/SKILL.md`](aimo/SKILL.md) 里的信息源和人物名单。

## 贡献

欢迎提 Issue 反馈问题，或直接提 PR。详见 [CONTRIBUTING.md](CONTRIBUTING.md)。

## 许可

[MIT](LICENSE)
