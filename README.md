# 共创式视觉情绪板 · Visual Direction Moodboard

围绕关键词和已有想法寻找真实设计，一起看图、选图、讨论，再把共同形成的判断整理成情绪板。

**关键词与已有想法 → 真实参考 → 候选图库 → 讨论与补搜 → 情绪板。**

已有具体设计问题时，也可以先研究局部方法，按需试做，再看结果讨论。找图与看图本身就是产出。

## 能做什么

- 按关键词展示真实作品，保留稳定编号、来源和完整项目入口。
- 提供可回看的候选图库，支持跨组比较、选图和反馈；推荐之外的候选也能找到。
- 随反馈修订搜索路线，区分用户选择、Agent 推荐和待验证推断。
- 按需比较图像处理、裁切或字图关系，用小规模试样检验方向，再整理情绪板或视觉规则。

## 下载与安装

到 [Releases](https://github.com/buttonsprite/visual-direction-moodboard/releases) 下载对应平台的 ZIP。

### Codex / 标准 Skill 目录

下载 `visual-direction-moodboard-v0.1.0.zip`，解压后将 `visual-direction-moodboard` 文件夹放入当前环境的 Skills 目录。Codex 默认目录是 `~/.codex/skills/`；设置了 `CODEX_HOME` 时使用其下的 `skills/`。已有同名 Skill 时先保留旧版本，再替换。

文件夹中应直接包含 `SKILL.md`、`references/` 和 `agents/`。重新加载技能或开启新任务后使用。

### WorkBuddy

下载 `visual-direction-moodboard-workbuddy-v0.1.0.zip`，用于支持 ZIP 的技能导入或开放平台提交。该包按 [WorkBuddy 官方技能规范](https://open.workbuddy.cn/docs/skill) 补充中英文描述、版本和作者字段，并适配资源引用。

WorkBuddy 专用包与标准包使用同一套流程；平台解析、实际运行和市场审核状态以 WorkBuddy 为准。提供安装包不代表已在市场上架。

## 开始使用

```text
使用 visual-direction-moodboard。我的项目是一个独立咖啡品牌，
已经有“温暖、粗粝、手工”的感觉。先围绕这些词找真实设计，
展示可浏览、可回看来源的候选图库，和我看图讨论后再整理方向。
```

```text
使用 visual-direction-moodboard。我已经有几张喜欢的封面参考。
先研究它们的图像处理与字图关系；我选完参考后，
再拿同一张照片做少量对照试样，看看哪些方法适合我的素材。
```

在 Codex 中也可以用 `$visual-direction-moodboard` 明确调用。

## 运行条件与边界

这是工作流程 Skill，包含指令、参考流程和记录模板。候选图库和试样由运行它的 Agent 根据项目制作，包内没有固定图库应用或图片处理引擎。

Agent 需要可用的搜索/浏览与图片查看能力；制作 HTML 或试样时还需要相应文件输出、预览或图像制作工具。没有绑定付费服务、特定模型或其他私有 Skill。工具不可用时应说明研究或验证缺口。

本版本基于真实项目使用反馈整理，并完成文件格式、引用与打包检查。跨 Agent 的表现、WorkBuddy 运行效果仍需实际试用；Skill 不保证一次生成完整品牌系统。收集的第三方作品需保留来源，其使用权不包含在本仓库许可证中。

## 内容

- [SKILL.md](SKILL.md)：入口与共创原则。
- [标准流程](references/standard-workflow.md)：搜图、讨论、整理及可选试做。
- [记录模板](references/deliverable-templates.md)：候选、反馈、对照与交接。

欢迎通过 [Issues](https://github.com/buttonsprite/visual-direction-moodboard/issues) 反馈触发方式、Agent 环境、停在哪一步，以及预期与实际结果。请勿附带私人项目资料或无权公开的参考图。

## License

MIT，见 [LICENSE.txt](LICENSE.txt)。

---

A collaborative moodboard workflow for agents: research real design references, browse and discuss candidates, refine the search, and synthesize a visual direction. Optional focused trials help test ideas before committing. Instructions are primarily in Chinese; standard and WorkBuddy packages are provided separately.
