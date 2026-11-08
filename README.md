# 校园报修系统（Campus Repair System）

这是一个**示例项目**，演示如何借助 AI 编程工具与「毕业设计技能包」辅助完成一篇完整的计算机类本科毕业设计。

示例以校园报修系统为载体，覆盖从选题到答辩的全流程，展示每个阶段该用哪个技能、如何与 AI 协作、产出什么材料。

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

1. **安装技能**：在项目中执行下方安装命令，为你的 AI 工具装配技能包。
2. **按阶段推进**：进入每个阶段时，直接告诉 AI 你要做的事（如"帮我根据任务书写开题报告"），对应技能会被自动调用。
3. **人机协作**：AI 负责起草、检查、答疑；你负责决策、修改和确认，所有关键结论由你拍板。
4. **沉淀材料**：每阶段产出的文档都保留在仓库中，作为论文和答辩的证据链。

## 毕业设计技能

### 安装技能包

```bash
# 推荐使用 WorkBuddy 擅长写文档，界面友好操作简单，技能、专家、连接器生态丰富。
npx @dedeguo/graduation-design-skills --tool workbuddy

# trae IDE 擅长代码生成，界面友好操作简单, 插件市场有一些插件可以辅助开发
npx @dedeguo/graduation-design-skills --tool trae

# claude code 擅长代码生成
npx @dedeguo/graduation-design-skills --tool claude

# codex
npx @dedeguo/graduation-design-skills --tool codex

```

### 更新技能包

```bash
npx @dedeguo/graduation-design-skills@latest --tool claude
```

更新时传入安装时使用的 `--tool`。重新安装时，只会覆盖当前技能包中的同名 Skill。

### 卸载技能包

```bash
npx @dedeguo/graduation-design-skills --tool codex --uninstall
```

卸载时传入安装时使用的 `--tool`。卸载器会删除以下内容。

* 本技能包中包含的同名 Skill
* 选择 TRAE 时，由本安装器生成的 Rule 文件

不会删除用户自己创建的其他 Skills 和 Rules。