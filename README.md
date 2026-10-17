# Grok Bots for DeepSeek Harness（中文版）

90 个智能体预设，转换自 [Grok Bot 市场](https://x.ai/bot/marketplace)，打包为 DeepSeek Harness 插件包。每个插件包包含一个智能体预设及该机器人的技能；只安装你想要的机器人。

浏览：https://harlucy.github.io/grok-bots-for-deepseek-harness/

> 本仓库是原项目的镜像：站点页面、README 与插件元数据已汉化，机器人内部的技能文档与人格提示词保留英文原文。

## 从「发现」标签页安装

1. 在 dsh 中打开「插件」，在「实验性插件」旁选择「更多」，打开「自定义插件市场」。
2. 在「发现」标签页添加此索引：`https://harlucy.github.io/grok-bots-for-deepseek-harness/index.json`
3. 搜索或筛选，选择机器人，点击「安装」。
4. 新建会话，在预设选择器中选择该机器人。

## 从命令行安装

```
npx -y @deepseek-ai/dsh plugin --profile web add "git+https://github.com/Harlucy/grok-bots-for-deepseek-harness.git#main&path:/bots/human-copywriter"
```

把 slug 换成 `bots/` 下任意文件夹名。需要 PATH 中有 pnpm。

## 每个插件包包含什么

- `cordis.patch.yml` 插入一行 `@deepseek-ai/dsh-agent-preset`：内置标准预设的工具，加上该机器人的人格，以及 `skills.mjs`。
- `skills.mjs` 把机器人的 `skills/*/SKILL.md` 注册到该预设的技能注册表，因此这些技能只对该机器人生效。
- `setup-prompt.md` 通过 `schedule_create` 创建机器人的定时任务（需先启用「插件 > 官方 > 自动化任务」）。

## 致谢与条款

这里的每个模板都由其 README 中署名的创作者编写，并发布在 x.ai 上。本仓库只是把它们重新打包为 DeepSeek Harness 格式。再分发前请查看市场条款。

## 重新构建

由 https://github.com/akloster/grok-bot-marketplace-tools 中的 `gen_dsh_market.py` 生成（完整地从 Grok 市场生成到本仓库的流水线见该仓库 README）。提交机器人改动后运行 `./build_index.py` 并提交 `docs/`。
