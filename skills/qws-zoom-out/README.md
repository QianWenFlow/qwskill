# qws-zoom-out

这次开源的是一个「升维 Skill」，它是 [qwskill](../../README.md) 中的一个 Skill

和 AI 反复修改、越改越不满意时，调用它。它帮你跳出当前的局部视角，站到更高的维度看这件事，找到正确的解决办法，并在同一条回复里给出改法

英文名 Zoom Out 是镜头拉远的意思：贴得太近，只能看到眼前正在改的那一处；拉远以后，才看得见它在整件事里的位置，问题真正出在哪里

改文案、选封面文字、定视频框架、修一套规则或流程，都可以用。它不替你写完整的文章或方案，只负责把你从局部带出来，再把改法交回原来的任务

## 它能解决哪些问题

- 同一个地方改了很多遍还是不对：问题可能不在这个地方，而在整篇文案的结构，甚至内容和账号的定位；
- 规则、Skill 或流程补丁越打越多，越用越不顺手：该调整的可能是整体的做法；
- 同一个毛病改好了又出现：你修的可能只是它冒出来的地方；
- 几个 AI 各说各的，或者讨论了好几轮还是回到原点：你们比较方案的标准可能一直在变

任何时候觉得自己被困在一个局部里，都可以调用它

## 你会得到什么

一次调用得到一条完整回复，包含四部分：

- **卡在哪**

  你到底困在哪，以及最关键的一条依据。这类问题已有成熟做法时，直接说出做法；没有把握时，说明问题类型并给出可以搜索的关键词，方便你继续查找理论和方法

- **原答案保留还是替换**

  先找出开始绕圈子之前的那一版答案。新答案只有在具体事实或你的诉求上更好时才会替换它，否则保留原答案

- **改法**

  小改动（一句话、一处指代、一个标题）直接给一到两个候选，并说明改哪里、怎么检查改完是否成立。大改动（换目标、换定位、换框架）直接告诉你该往哪个方向调整；需要你拍板的取舍只问一个问题，你选定后再给具体改法

  改法精准落在真正出问题的那一处，顺带发现的其他问题只列为可选，你认可的内容都保留

- **停在哪**

  一句话说明为什么查到这里就停：再往上会改变你原来的问题或已经定好的定位

## 使用

```text
/qws-zoom-out
```

也可以直接说「升维」，或者通过 [qwskill 统一入口](../../README.md#使用) `/qws` 调用

例如：

> /qws-zoom-out 这句话里的「这」指代不明，已经改了三版还是不对。

> /qws-zoom-out 这条推文在几个 AI 之间改出了好几个方向，我拿不定主意，看看卡在哪。

> /qws-zoom-out 这个 Skill 的规则越加越多，结果还是不满意。AI 又建议加一条规则，要不要加？

安装与更新见 [qwskill 首页](../../README.md#安装与更新)

## 它怎样工作

- **先找出原答案**

  把你认可过的版本，或者开始绕圈子之前的那一版，作为对照的基准。后来的讨论批评过它，不等于它被推翻

- **先看出你困在哪种局部**

  对照常见的绕圈子原因判断这次属于哪一种，例如每次只换说法、没换共同前提，没有固定的评价标准，补丁越加越多却不收敛。不在常见类型里时，也会说出这是哪一种

- **一次查到最终层级**

  往上检查到「再往上就会改变你原来的问题或已经定好的定位」为止，交付前先确认再调用一次也不会得出不同答案，避免你反复调用

- **缺信息时先给判断**

  先从对话和你提供的材料中找；找不到时，按最可能的情况给出判断并写明假设，最后只问一个带选项的问题

## 边界与隐私

你明确要求时它才会深入检查：说「升维」、「从全局看」、「这是不是局部问题」这类话，或者调用 `/qws-zoom-out`。你在同一件事上反复修改仍不满意时，Agent 识别到后会在回复末尾提醒一句可以升维，不打断原来的任务

价值取舍由你决定。已经发生的执行错误，例如文件没保存对、命令执行失败，不属于它处理的范围

它读取当前对话、你提供的材料，以及判断需要时项目里已有的相关资料（例如账号定位文档、已发布内容清单）。它不会把分析过程写进你的文稿或长期档案，也不需要联网

## 设计依据（不参与每次运行）

以下内容说明这些判断规则的来源，不参与每次运行，也不会出现在回复里

### 重新定义问题

- Donald Schön 的反思性实践与问题设定，用于检查当前框架本身是否需要重设，并让事实反馈检验新框架，参考 [MIT 反思性实践课程书目](https://ocw.mit.edu/courses/11-965-reflective-practice-an-approach-for-expanding-your-learning-frontiers-january-iap-2007/pages/readings/)
- Chris Argyris 的双环学习，用于检查支配行动的目标、规则和前提，参考 [Double Loop Learning in Organizations](https://hbr.org/1977/09/double-loop-learning-in-organizations)
- Horst Rittel 与 Melvin Webber 的棘手问题，用于提醒问题定义与解法会互相影响，参考 [Dilemmas in a General Theory of Planning](https://doi.org/10.1007/BF01405730)

### 目标与取舍

- Ralph Keeney 的价值导向思考，用于区分目的与手段、比较方案，参考 [Applying Value-Focused Thinking](https://scholars.duke.edu/publication/780161)

### 系统范围与停止

- Donella Meadows 的系统杠杆点，用于判断该在规则、结构、信息反馈还是目标上介入，参考 [Leverage Points](https://donellameadows.org/archives/leverage-points-places-to-intervene-in-a-system/)
- Herbert Simon 的近似可分解系统，用于判断什么时候局部处理就足够、可以停止扩展，参考 [The Architecture of Complexity](https://www.andrew.cmu.edu/course/15-440/assets/READINGS/simon-architecture-of-complexity-1962.pdf)
- NASA 系统工程手册，用于父级需求追溯和整体验收，参考 [NASA Systems Engineering Handbook](https://www.nasa.gov/wp-content/uploads/2018/09/nasa_systems_engineering_handbook_0.pdf)

### 内容与账号

- Maxwell McCombs 与 Donald Shaw 的议程设置，用于判断一条内容在账号长期议程中承担什么作用，参考 [The Agenda-Setting Function of Mass Media](https://doi.org/10.1086/267990)

这些依据解释判断方法为什么成立，不能证明某一次的具体改法一定正确。每次的结论仍要回到你的原始事实和诉求核对

## 项目信息与许可证

作者、致谢和许可证见 [qwskill 首页](../../README.md#项目信息)。本 Skill 与整个仓库一样采用 [CC BY-NC 4.0](../../LICENSE) 许可证
