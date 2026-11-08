# 校园报修系统（Campus Repair System）

这是一个**示例项目**，演示如何借助 AI 编程工具与「毕业设计技能包」，辅助完成一篇完整的计算机类本科毕业设计。

示例以校园报修系统为载体，覆盖从选题到答辩的全流程，展示每个阶段该用哪个技能、如何与 AI 协作、产出哪些材料。

在 AI 工具的选择上，推荐在 Windows 系统下使用 WorkBuddy，它的文档写作效果出众；系统开发、编码与测试同样可以用 WorkBuddy 完成，也可选择 Trae IDE、Claude Code、Codex 等其他 AI 编程工具。

## 全流程与技能对照

| 阶段 | 产出材料 | 对应技能 |
| ---- | ---- | ---- |
| 选题 | 任务书、题目论证 | `topic-selection` |
| 开题 | 开题报告、答辩 PPT、模拟问答 | `proposal-defense` |
| 需求分析 | 需求分析说明书（角色、场景、验收标准） | `requirements-analysis` |
| 系统设计 | 系统设计说明书（架构、数据库、UI 原型） | `system-design` |
| 开发测试 | 按里程碑迭代的可运行系统 + 测试记录 | `system-development` |
| 论文撰写 | 论文章节初稿 | `thesis-writing` |
| 论文评阅 | 修改批注、评阅报告、答辩前检查 | `thesis-review` |

## 推荐工作流

1. **安装技能**：在项目中执行下方安装命令，为 AI 工具装配技能包。
2. **按阶段推进**：进入某一阶段时，直接用自然语言说明你的目标（例如"帮我根据任务书写开题报告"），对应的技能便会被自动调用。
3. **人机协作**：AI 负责起草、检查与答疑，你负责判断、修改与确认，关键结论由你把关。
4. **沉淀材料**：每个阶段的产出都保留在仓库中，形成支撑论文与答辩的完整证据链。

## 毕业设计技能

### 安装技能包

```bash
# WorkBuddy：文档写作是强项，界面友好、操作简单，技能、专家与连接器生态丰富
# 在 Windows 系统下，文档生成效果更佳
npx @dedeguo/graduation-design-skills --tool workbuddy

# Trae IDE：擅长代码生成，界面简洁易用，插件市场另有插件可辅助开发
npx @dedeguo/graduation-design-skills --tool trae

# Claude Code：擅长代码生成
npx @dedeguo/graduation-design-skills --tool claude

# Codex
npx @dedeguo/graduation-design-skills --tool codex

```

### 更新技能包

```bash
npx @dedeguo/graduation-design-skills@latest --tool claude
```

更新时请传入安装时所用的 `--tool`。重新安装只会覆盖本技能包中的同名 Skill，不会影响其他内容。

### 卸载技能包

```bash
npx @dedeguo/graduation-design-skills --tool codex --uninstall
```

卸载时同样需要传入安装时所用的 `--tool`。卸载器会删除以下内容：

* 本技能包所包含的同名 Skill
* 若选择 TRAE，还会删除由本安装器生成的 Rule 文件

你自己创建的其他 Skills 与 Rules 不会被删除。