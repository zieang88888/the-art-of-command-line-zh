# 第三方声明与版权说明（THIRD PARTY NOTICES）

本仓库 **the-art-of-command-line-zh** 是对下列开源项目的**中文导读索引（index / reading guide）**，并非其译文或正文复制。本仓库**不包含源项目 README 的正文内容**，仅提供章节中文译名、主题索引与高频命令中文说明，便于中文读者快速定位、跳转回源项目阅读原文。

## 1. 源项目署名

- **源项目**：[jlevy/the-art-of-command-line](https://github.com/jlevy/the-art-of-command-line)
- **作者**：Joshua Levy（GitHub: [@jlevy](https://github.com/jlevy)，Holloway）
- **贡献者与译者**：见源仓库 `AUTHORS.md`——「This work is the result of many authors and translators.」部分内容最初发表于 Quora，后迁移至 GitHub 并由社区贡献者持续改进。
- **默认分支**：`master`
- **本仓定位**：中文速查索引 / 导读，不含源文正文。

## 2. 源项目许可状态（如实记录）

- **源仓库根目录无独立 LICENSE 文件**（在线核实，2026-10-06）。
- 源项目 README 尾部设有 `## License` 章节，实测原文如下（2026-10-06 抓取 `https://raw.githubusercontent.com/jlevy/the-art-of-command-line/master/README.md` 确认）：

  > "This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/)."

  并配有徽章 `https://i.creativecommons.org/l/by-sa/4.0/88x31.png`。

- **重要说明（与任务预设的差异，如实披露）**：源 README 尾部 License 章节实测声明的是 **Creative Commons Attribution-ShareAlike 4.0（CC BY-SA 4.0）**，其链接为 `by-sa/4.0`，即「署名—相同方式共享」，**并不包含 NonCommercial（非商业）要素**。也就是说，源项目 README 自我声明的许可证为 **CC BY-SA 4.0**，而非 CC BY-NC-SA 4.0。
- 本仓库按维护者指示，将其导读索引内容以 **CC BY-NC-SA 4.0** 发布（见本仓 `LICENSE`）。由于本仓仅为索引/导读、不含源文正文，该选择由本仓维护者自行承担；如需引用源项目正文，请严格以源项目 README 尾部声明的 **CC BY-SA 4.0** 为准，并回溯访问 https://creativecommons.org/licenses/by-sa/4.0/ 确认最新条款。

## 3. 星数与统计口径（核实日期：2026-10-06）

- **GitHub Stars**：**140,756**（GitHub REST API `https://api.github.com/repos/jlevy/the-art-of-command-line` 字段 `stargazers_count`，2026-10-06 实测；README 标题使用约数「140,000+」，徽章使用精确值 140,756）。
- **统计对象**：源仓库 `master` 分支 `README.md`（单页文档，全文 10,205 字符，分页读满）。
- **章节数 = 9**：统计 `##` 二级标题中包含实质内容的章节，依次为 Meta / Basics / Everyday use / Processing files and data / System debugging / One-liners / Obscure but useful / macOS only / Windows only。**排除** `## More resources`（外部资源链接列表）、`## Disclaimer`（免责声明）、`## License`（许可声明）三个收尾章节。
- **技巧/命令条目数 = 211**：逐章统计该章节下的**顶层无序列表项**（`- ` 开头的一级 bullet），嵌套子项不计入；各章计数为：
  - Meta：6（Scope 4 + Notes 2，均为说明性文字，**不计入 211 技巧总数**）
  - Basics：12
  - Everyday use：44
  - Processing files and data：35
  - System debugging：20
  - One-liners：8
  - Obscure but useful：72
  - macOS only：7
  - Windows only：13（含其子节 Ways to obtain Unix tools 4 + Useful Windows tools 3 + Cygwin tips 6）
  - 合计：12 + 44 + 35 + 20 + 8 + 72 + 7 + 13 = **211**
- **平台数 = 3**：Linux（主体）、macOS（专章）、Windows（专章）。
- 以上计数由人工逐条核对源 README 全文得出，统计日期 2026-10-06；后续源仓库若更新，数字可能变化，请以源仓库实测为准。

## 4. 本仓库内容

- 本仓库仅产出：中文 README 导读、`cheatsheet-index.md` 全量章节中文索引、3 张视觉 SVG、本声明与 CC BY-NC-SA 4.0 LICENSE。
- 所有命令名称、技巧条目均来自源 README 真实内容；中文说明为导读性翻译概括，**不替代源文原文**。

## 5. 致谢

向 Joshua Levy 及 `the-art-of-command-line` 全体贡献者、译者致敬——这份单页文档已成为命令行领域的极客圣经，惠及全球数百万开发者。
