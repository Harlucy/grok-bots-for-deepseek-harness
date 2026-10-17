# Grok Bots 中文插件源（DeepSeek Harness）

[Grok Bots for DeepSeek Harness](https://brokep.github.io/grok-bots-for-deepseek-harness/index.json) 插件索引的**中文翻译版**：90 个机器人预设的标题、描述、分类名、标签名全部汉化，字段结构与原始文件一致，可直接当作插件源使用。

## 插件源地址

已启用 GitHub Pages（Deploy from a branch → `main` / `root`），插件源地址：

```
https://harlucy.github.io/grok-bots-for-deepseek-harness/index.json
```

备用 raw 地址（不经 Pages，推送后立即可用）：

```
https://raw.githubusercontent.com/Harlucy/grok-bots-for-deepseek-harness/main/index.json
```

## 仓库内容

| 文件 | 说明 |
| --- | --- |
| `index.json` | 中文插件索引（即插件源本身）：仅翻译 `title` / `description` 及分类、标签、排序项的展示名；`name`、`author`、`homepage`、`repository`、`keywords`、`versions`、`dist-tags` 等全部保持原样 |
| `preview.html` | 中文可视化预览页：按分类浏览 90 个机器人，支持中文搜索，双击即可用浏览器打开 |
| `README.md` | 本说明 |

原始英文索引未纳入仓库（本地保留为 `index.en.json` 仅供对照），可从上方上游地址获取。

## 翻译说明（注释）

- 共 **90 个机器人预设、10 个分类、450 项技能**。
- **只做翻译**：仅 `title`、`description` 以及 `metadata.categories`、`metadata.labels`、`metadata.sortKeys` 里的展示名被翻译，其余字段逐字节保持原样。
- **品牌与产品名保留原文**：Slack、Notion、Figma、Salesforce、Gong、Granola、X、Google Ads 等；纯人名类机器人名（Alfred、Cooper、Flora、Imogen、frank 等）也保留原名。
- **原文截断**：上游 JSON 中有 5 条描述本身在 300 字符处被截断（`dr eggbot`、`last30days`、`Stalk Bot`、`Webby`、`WTD`），中文版在对应位置以 `……` 标记截断，未补写原文没有的内容。
- **完整性校验**：已用脚本校验——除上述展示文本外，`index.json` 与原始英文索引的结构、字段顺序、取值完全一致（90 个插件一一对应，无增删）。
- 翻译时保留中文标点与英文空格排版（如「AI 助手」「Google Sheets」），便于阅读。
