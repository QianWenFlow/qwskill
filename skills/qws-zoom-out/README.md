# qws-zoom-out

这次开源的是一个「升维 Skill」，它是 [qwskill](../../README.md) 中的一个 Skill

你反复修改、越改越不满意的时候，可以调用它。它先检查你的问题本身问得对不对，再帮你跳出当前的局部视角，站到更高的维度看这件事，找到正确的解决办法，并在同一条回复里给出改法

英文名 Zoom Out 是镜头拉远的意思：贴得太近，只能看到眼前正在改的那一处；拉远以后，才看得见它在整件事里的位置，问题真正出在哪里

改文案、选封面文字、定视频框架、做 Skill、修一套规则或流程，都可以用。它不替你写完整的文章或方案，只负责把你从局部带出来，再把改法交回原来的任务

## 它能解决哪些问题

- 问题本身问得不对：照这个问法做到最好，也得不到你想要的结果。它会指出断点在哪，给出正确的问题和答案；问题问对了，就直接回答；
- 同一个地方改了很多遍还是不对：问题可能不在这个地方，而在整篇文案的结构，甚至内容和账号的定位；
- 规则、Skill 或流程补丁越打越多，越用越不顺手：该调整的可能是整体的做法；
- 同一个毛病改好了又出现：你修的可能只是它冒出来的地方；
- 几个 AI 各说各的，或者讨论了好几轮还是回到原点：你们比较方案的标准可能一直在变；
- 一直在加做法，却越做越糟：比如优惠一轮接一轮地加、规则一条接一条地补，有些做法其实可以不要；
- 两个要求互相打架：顾了这头就丢了那头，怎么折中都不满意；
- 不知道问题到底出在哪：改了很多遍，说不清哪里不对，最后只能将就着定下来

不限领域：写作、内容、经营、管理、搭建 Skill 和工作流，任何时候觉得自己被困在一个局部里，都可以调用它

## 你会得到什么

一次调用得到一条完整回复：你的问题卡在哪、哪些做法可以不用再做、接下来具体怎么改。问题本身问偏了，它会告诉你更该问什么，并直接回答。你已有的稿子和方案，会保留你原来的判断，只改真正出问题的那一处

## 使用

```text
/qws-zoom-out
```

也可以直接说「升维」，或者通过 [qwskill 统一入口](../../README.md#使用) `/qws` 调用

例如：

> /qws-zoom-out 这句话里的「这」指代不明，已经改了三版还是不对。

> /qws-zoom-out 这条推文在几个 AI 之间改出了好几个方向，我拿不定主意，看看卡在哪。

> /qws-zoom-out 这个 Skill 的规则越加越多，结果还是不满意。AI 又建议加一条规则，要不要加？

> /qws-zoom-out 账号涨粉停了，我把更新从一周三更加到五更，数据还是往下走，要不要干脆改成日更？

回答比较简短时，可以接着问一句「还有别的办法吗」

安装与更新见 [qwskill 首页](../../README.md#安装与更新)

## 它怎样工作

- **先看问题本身问得对不对**

  问对了就直接回答；问偏了，就告诉你更该问什么

- **看哪些做法可以不要**

  你打算做的事、方案里默认必需的步骤，逐个看：不做它，你要的结果能不能用别的办法达到

- **找到问题出在哪一层**

  前提（这件事该不该这样做）、目标和标准（要什么、怎样算好）、规则和结构（谁做什么、怎么交接），还是只是措辞和数量。反复修改过的，还会说出你困在哪一类局部，以及这类问题已有的成熟做法

- **找不到突破时换个角度**

  两个要求打架时，按时间、对象或条件把它们分开；方案看着都对却没把握时，先假设它失败了，倒推原因；改过很多轮的东西，假设从头开始会怎么设计

- **一次给出最终结果**

  缺信息时按最可能的情况先给判断，需要你拍板的只在最后问一个问题。你再说一次「升维」、又没有新情况时，沿用原来的答案

## 边界与隐私

调用它就会走完整个检查并给出最终结果，不需要再说「升维」：用 `/qws-zoom-out`、`$qws-zoom-out` 或 Skill 链接调用，或者说「升维」、「从全局看」、「这是不是局部问题」这类话都可以。你在同一件事上反复修改仍不满意时，Agent 识别到后会在回复末尾提醒一句可以升维，不打断原来的任务

价值取舍由你决定。已经发生的执行错误，例如文件没保存对、命令执行失败，不属于它处理的范围

它读取当前对话、你提供的材料，以及判断需要时项目里已有的相关资料（例如账号定位文档、已发布内容清单）。它不会把分析过程写进你的文稿或长期档案，也不需要联网

## 设计依据（不参与每次运行）

以下内容说明这些判断规则的来源，不参与每次运行，也不会出现在回复里

### 判断问题对不对

- Ian Mitroff 的第三类错误（精确地解决了错误的问题），用于说明为什么要先判断问题、再作答，参考 [Type III error](https://en.wikipedia.org/wiki/Type_III_error)
- Paul Watzlawick、John Weakland、Richard Fisch 的一阶与二阶改变，用于判断「做法本身维持了问题」，参考 [Change: Principles of Problem Formation and Problem Resolution](https://www.goodreads.com/book/show/9963373)
- Jacques Hadamard 的适定问题，用于判断一个问题有没有确定的答案，参考 [Well-posed problem](https://en.wikipedia.org/wiki/Well-posed_problem)
- 语言哲学中的预设失败，用于检查问题里藏着的错误前提，参考 [Presupposition Verification for Question-Answering](https://arxiv.org/pdf/2101.00391)
- Thomas Wedell-Wedellsborg 的问题重构，用于先设定问题、再求解的顺序，参考 [Are You Solving the Right Problems?](https://hbr.org/2017/01/are-you-solving-the-right-problems)
- Donald Schön 的反思性实践与问题设定，用于检查当前框架本身是否需要重设，并让事实反馈检验新框架，参考 [MIT 反思性实践课程书目](https://ocw.mit.edu/courses/11-965-reflective-practice-an-approach-for-expanding-your-learning-frontiers-january-iap-2007/pages/readings/)
- Chris Argyris 的双环学习，用于检查支配行动的目标、规则和前提，参考 [Double Loop Learning in Organizations](https://hbr.org/1977/09/double-loop-learning-in-organizations)
- Horst Rittel 与 Melvin Webber 的棘手问题，用于提醒问题定义与解法会互相影响，参考 [Dilemmas in a General Theory of Planning](https://doi.org/10.1007/BF01405730)
- Ralph Keeney 的价值导向思考，用于区分目的与手段、找到根本目标，参考 [Applying Value-Focused Thinking](https://scholars.duke.edu/publication/780161)
- Clayton Christensen 的「用户要完成的任务」，用于找到手段背后的需要，参考 [Know Your Customers' Jobs to Be Done](https://hbr.org/2016/09/know-your-customers-jobs-to-be-done)
- George Pólya 的《怎样解题》，用检查特殊情形和极端情形来检验猜想，参考 [How to Solve It](https://en.wikipedia.org/wiki/How_to_Solve_It)
- Robert Lucas 的卢卡斯批判，用于判断其他参与者适应之后方案是否失效，参考 [Econometric Policy Evaluation: A Critique](https://ideas.repec.org/a/eee/crcspp/v1y1976ip63-64.html)

### 哪些做法可以不要

- Gabrielle Adams 等人关于减法的实验，发现人在改进事物时容易只想到增加、忽略删减，用于主动检查哪些做法可以不要，参考 [People systematically overlook subtractive changes](https://pubmed.ncbi.nlm.nih.gov/33828317/)
- Stellan Ohlsson 的表征转换理论，用于说明去掉自己默认的限制、把当成一整块的东西拆开，是产生突破的两种方式，参考 [Constraint relaxation and chunk decomposition in insight problem solving](https://www.kognition.uni-koeln.de/literature/Knoblich_etal_1999.pdf)
- Jason Pierce 与 Herman Aguinis 的过犹不及效应，用于判断手段做满后是否起反作用，参考 [The Too-Much-of-a-Good-Thing Effect in Management](https://homepages.se.edu/cvonbergen/files/2012/12/The-Too-Much-of-a-Good-Thing-Effect-in-Management.pdf)

### 问题出在哪一层、查到哪里停

- Donella Meadows 的系统杠杆点，用于判断该在规则、结构、信息反馈还是目标上介入，参考 [Leverage Points](https://donellameadows.org/archives/leverage-points-places-to-intervene-in-a-system/)
- Jens Rasmussen 的抽象层级，用于从目的到具体做法分层看一个系统，参考 [Work domain analysis](https://en.wikipedia.org/wiki/Work_domain_analysis)
- Jens Rasmussen 关于动态社会中风险管理的研究，用于提醒问题常出在层与层的交接上，参考 [Risk management in a dynamic society](https://orbit.dtu.dk/en/publications/risk-management-in-a-dynamic-society-a-modelling-problem/)
- David Parnas 的模块分解准则，用于把经常变化的部分和不常变的部分分开，参考 [On the criteria to be used in decomposing systems into modules](https://blog.acolyer.org/2016/09/05/on-the-criteria-to-be-used-in-decomposing-systems-into-modules/)
- Stafford Beer 的可行系统模型，用于按决策范围和时间尺度拆分职责，参考 [Viable System Model](https://ieeemilestones.ethw.org/w/images/7/73/Viable_system_Model.pdf)
- RFC 3439 中「分层被认为有害」一节，用于提醒层分得太多也会失败，参考 [RFC 3439](https://datatracker.ietf.org/doc/rfc3439/)
- Anthropic 的 Building effective agents，用于判断 AI 任务什么时候才需要拆给不同的智能体，参考 [Building effective agents](https://www.anthropic.com/research/building-effective-agents)
- Herbert Simon 的近似可分解系统，用于判断什么时候局部处理就足够、可以停止扩展，参考 [The Architecture of Complexity](https://www.andrew.cmu.edu/course/15-440/assets/READINGS/simon-architecture-of-complexity-1962.pdf)
- NASA 系统工程手册，用于父级需求追溯和整体验收，参考 [NASA Systems Engineering Handbook](https://www.nasa.gov/wp-content/uploads/2018/09/nasa_systems_engineering_handbook_0.pdf)
- Russell Ackoff 的四种处理方式（搁置、应付、求解、消解），用于决定投入多大力气处理，参考 [The Art of Problem Solving](https://www.wiley-vch.de/en/areas-interest/finance-economics-law/the-art-of-problem-solving-978-0-471-85808-9)

### 找不到突破时的角度

- Genrich Altshuller 的 TRIZ 分离原理，用于按时间、空间、条件或层级把互相冲突的要求分开，参考 [TRIZ Method](https://thinkinsights.net/consulting/triz-method)
- Gary Klein 的事前验尸，用于先假设方案失败、倒推原因，参考 [Pre-mortem](https://en.wikipedia.org/wiki/Pre-mortem)
- Lee Bolman 与 Terrence Deal 的四框架，用于从分工、人、利益和意义几个角度看同一件事，参考 [Four-Frame Model](https://www.businessballs.com/leadership-styles/four-frame-model-bolman-deal/)
- Russell Ackoff 的理想化设计与 Genrich Altshuller 的 TRIZ 理想最终结果，用于设想不用现有做法、从头设计时会怎样，参考 [Idealized Design](https://isfcolombia.uniandes.edu.co/images/2020-intersemestral/23_de_junio/ackoff1993.pdf)

### 内容与账号

- Maxwell McCombs 与 Donald Shaw 的议程设置，用于判断一条内容在账号长期议程中承担什么作用，参考 [The Agenda-Setting Function of Mass Media](https://doi.org/10.1086/267990)

这些依据解释判断方法为什么成立，不能证明某一次的具体改法一定正确。每次的结论仍要回到你的原始事实和诉求核对

## 项目信息与许可证

作者、致谢和许可证见 [qwskill 首页](../../README.md#项目信息)。本 Skill 与整个仓库一样采用 [CC BY-NC 4.0](../../LICENSE) 许可证
