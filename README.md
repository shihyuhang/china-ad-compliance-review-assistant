# 中国广告合规审核助手

面向中国市场的广告发布前合规风险筛查 Skill，适用于广告文案、图片、视频、直播脚本、详情页和落地页。

它会先回答“能不能发”，再输出：

- **必改**：已能确认的强制性风险
- **需补证**：主张可能成立，但证据尚不足
- **建议**：不当然违法，但容易误导或引发平台风险

覆盖绝对化用语、功效与数据宣称、价格与促销、广告可识别性、代言、行业资质、广告前置审查、AI 生成内容标识，以及医疗、药品、器械、保健食品、金融、教育、房地产等行业的常见风险。

## 重要边界

本项目用于初步风险筛查，不替代律师正式法律意见，也不保证离线规则始终保持最新。涉及重大投放、特管行业、争议性定性或高额责任时，应核对现行官方文本并由专业人员复核。

有联网或法规数据库时，应逐条核验法源；没有时，报告必须明确写明未做时效核验。

## 安装

将 `skill/china-ad-compliance-review` 目录复制到 Codex 的 Skills 目录，然后使用：

```text
使用 $china-ad-compliance-review 审核这份广告素材，先告诉我能不能发。
```

其他平台可以把 `skill/china-ad-compliance-review/prompts/universal.md` 用作系统指令。详细说明见 [安装文档](docs/installation.md)。

## 项目结构

```text
skill/china-ad-compliance-review/
├── SKILL.md
├── agents/openai.yaml
├── prompts/universal.md
└── references/
    ├── blind-spots.md
    ├── claim-matrix.md
    ├── industries.md
    ├── legal-sources.md
    ├── liability-scale.md
    └── output-format.md
```

公开版未打包来源不清或难以持续维护的大段协会、平台规则全文；动态规则统一从 `references/legal-sources.md` 的官方入口核验。

## 法源与更新

- 核心法源入口见 [`legal-sources.md`](skill/china-ad-compliance-review/references/legal-sources.md)。
- 法源清单最后核对日期：**2026-10-28**。
- 发现规则更新或错误，欢迎提交 Issue 或 Pull Request，并附官方来源。

## 许可证

原创代码、提示词、结构与说明文档采用 [MIT License](LICENSE)。引用的法律法规及官方文件仍按其各自法律属性与来源使用，项目不对第三方材料主张权利。

