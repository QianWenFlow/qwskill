# 方法依据与适用边界

本文件说明 `system-scope-model.md` 中各项判断方法的来源，运行时不读取。

理论用于支持上述判断动作，不用于证明 Skill 已有效；实际表现仍需行为验证。

- **Donald Schön，问题设定与反思性实践**：支持找断点和判定，并让事实反馈检验新框架；不意味着换一种说法就算进步。参见 *The Reflective Practitioner*，尤其 “The Structure of Reflection-in-Action”。[MIT 反思性实践课程书目](https://ocw.mit.edu/courses/11-965-reflective-practice-an-approach-for-expanding-your-learning-frontiers-january-iap-2007/pages/readings/)。
- **Ralph Keeney，价值导向思考**：从已确认的目标和必要条件逐项生成行动，再看条件之间需要怎样配合；生成和评价分开，防止只在最先出现的做法中挑选。Siebert 与 Keeney 的五项研究发现，用目标逐项、再成对地启发候选，比只增加思考时间更有助于形成好候选；研究对象是人类决策者，不能直接证明本 Skill 对模型有效。对应主文件第 3 步和系统模型第三节；其中手段—目标关系（每个手段服务于一个目标，去掉手段就回到目标另找手段）也用于第 2 步减法；不能凭目标推断未给出的事实，也不能保证找到唯一最优方案。[Value-focused thinking: Identifying decision opportunities and creating alternatives](https://www.sciencedirect.com/science/article/pii/0377221796000045)、[Creating More and Better Alternatives for Decisions Using Objectives](https://pubsonline.informs.org/doi/pdf/10.1287/opre.2015.1411)。
- **Gabrielle Adams 等，减法容易被忽略**：八组人类实验发现，未提示考虑删减时，参与者较少识别有益的删减方案。支持在行动方案生成前主动检查能否去掉现有手段；研究不决定具体该去掉哪一步，也不证明模型采用此提示后必然改善。删减对象由当前目标和手段关系确定，涵盖用户做法及 Agent 自设流程。[People systematically overlook subtractive changes](https://pubmed.ncbi.nlm.nih.gov/33828317/)。
- **Ronald Howard，策略生成表**：把不同决策处的动作组合成相互配合的完整方案，不让零散动作或方案名称冒充一条可执行路径。这里借用“组合成连贯方案”的方法，不要求运行时画表、穷举组合或强制多方案；具体组合必须符合事实、权限和参与者选择。对应主文件第 3 步的候选生成。[Decision Analysis: Practice and Promise](https://pubsonline.informs.org/doi/abs/10.1287/mnsc.34.6.679?journalCode=mnsc)。
- **Ronald Howard，决策敏感性分析**：检查不确定条件变化时适用做法是否会变化；对应主文件第 3 步形成路径时对适用条件的检查。这里借用的是定性比较，不要求每题建立数值模型，也不要求先删到一个方案；若路径本身遗漏，敏感性分析也无法替它发现新做法。[Proximal Decision Analysis](https://pubsonline.informs.org/doi/10.1287/mnsc.17.9.507)。
- **Chris Argyris，双环学习**：并入第一节的前提检查，检查支配行动的目标、规则和前提，不另设重复环节。[Double Loop Learning in Organizations](https://hbr.org/1977/09/double-loop-learning-in-organizations)。
- **Donella Meadows，系统杠杆点**：帮助识别目标、规则、信息流与反馈等介入位置；不默认越高层越适合当前任务。[Leverage Points](https://donellameadows.org/archives/leverage-points-places-to-intervene-in-a-system/)。
- **Horst Rittel 与 Melvin Webber，棘手问题**：问题定义与解法互相影响，当前问题可能是另一问题的症状；用于检验定义，不把所有任务判成无边界的复杂问题。[Dilemmas in a General Theory of Planning](https://doi.org/10.1007/BF01405730)。
- **Herbert Simon，近似可分解系统**：交互较弱时局部处理可以成立，支持保留原框架与停止扩展。[The Architecture of Complexity](https://www.andrew.cmu.edu/course/15-440/assets/READINGS/simon-architecture-of-complexity-1962.pdf)。
- **Maxwell McCombs 与 Donald Shaw，议程设置**：媒体反复强调什么、从什么角度讲，影响受众认为什么重要、怎样理解它；用于内容与账号任务的议程检查，不作为每条内容都要讲理论的理由。[The Agenda-Setting Function of Mass Media](https://doi.org/10.1086/267990)。
- **George Pólya，《怎样解题》**：检查特殊情形和极端情形来检验猜想；支持条件推演的整体做法，不意味着每个条件都要推。[How to Solve It](https://en.wikipedia.org/wiki/How_to_Solve_It)。
- **Russell Ackoff，理想化设计；Genrich Altshuller，TRIZ 理想最终结果**：前者从理想状态倒推，后者设想不消耗资源就实现功能；对应条件推演中把资源推到零、第 2 步减法（不要这个做法，它的作用还能不能实现），以及「阶梯之外的几个角度」中的从零设计（不动目标，假设从头开始会怎么设计）。本 Skill 不再要求把目标推到最强：「最强」没有定义，模型只能自己猜，会把用户的目标改得越来越极端。[Idealized Design: Creative Corporate Visioning](https://isfcolombia.uniandes.edu.co/images/2020-intersemestral/23_de_junio/ackoff1993.pdf)。
- **Jason Pierce 与 Herman Aguinis，过犹不及效应**：适度时有益的因素，超过某一点会转为有害；对应第 2 步减法时检查做法继续下去是否起反作用，结论作为提醒写在回答开头；须有事实显示已经做多才下此结论，不意味着每个手段都有这个拐点。[The Too-Much-of-a-Good-Thing Effect in Management](https://homepages.se.edu/cvonbergen/files/2012/12/The-Too-Much-of-a-Good-Thing-Effect-in-Management.pdf)。
- **Robert Lucas，卢卡斯批判**：行为者会根据新政策调整自己的行为，按旧行为估算的效果会失效；对应其他参与者推到完全适应，不意味着所有对象都会适应。[Econometric Policy Evaluation: A Critique](https://ideas.repec.org/a/eee/crcspp/v1y1976ip63-64.html)。
- **Ian Mitroff，第三类错误**：精确地解决了错误的问题；支持在交付前检查所回答的问题是否成立，不意味着每个问题都要怀疑。[Type III error](https://en.wikipedia.org/wiki/Type_III_error)。
- **Paul Watzlawick、John Weakland、Richard Fisch，《改变》**：一阶改变在原框架内调整，二阶改变改变框架本身；「更多同样的做法」会维持问题，解决办法本身可能成为问题；对应「做法维持了问题」的判据与改写方法，与双环学习一致。[Change: Principles of Problem Formation and Problem Resolution](https://www.goodreads.com/book/show/9963373)。
- **Jacques Hadamard，适定问题**：解存在、唯一、并连续依赖于输入；对应适定性的三项检查，「稳定」指答案对输入事实的敏感程度。[Well-posed problem](https://en.wikipedia.org/wiki/Well-posed_problem)。
- **预设失败与复杂问句（Strawson 等）**：问句预设了不成立的命题时，正面回答都会出错；对应前提检查。[Presupposition Verification for Question-Answering](https://arxiv.org/pdf/2101.00391)。
- **Russell Ackoff，四种处理方式**：搁置、应付、求解，以及改变系统或环境让问题不再出现（Ackoff 称为 dissolve）；对应主文件第 3 步的处理力度，与「问题是否成立」是两个维度。为避免与第 1 步「消解用户的问题」重名，本 Skill 把 dissolve 归入第 2 步减法，不称「消解」。“应付”只决定投入成本，不替代第 3 步检查决定结果的条件。[The Art of Problem Solving](https://www.wiley-vch.de/en/areas-interest/finance-economics-law/the-art-of-problem-solving-978-0-471-85808-9)。
- **Thomas Wedell-Wedellsborg，问题重构**：先设定问题、看框架外、重想目标，再求解；支持第 1 步的做法。[Are You Solving the Right Problems?](https://hbr.org/2017/01/are-you-solving-the-right-problems)。
- **Clayton Christensen，用户要完成的任务**：问「为了完成什么任务」找到手段背后的需要；对应根本目标与参与者目标。[Know Your Customers' Jobs to Be Done](https://hbr.org/2016/09/know-your-customers-jobs-to-be-done)。
- **NASA 系统工程手册**：支持父级需求追溯、接口检查和整体目标验收；用于系统范围路径，不作为一切问题都必须逐层上移的理由。[NASA Systems Engineering Handbook](https://www.nasa.gov/wp-content/uploads/2018/09/nasa_systems_engineering_handbook_0.pdf)。
- **Barbara Minto，金字塔原理**：结论先行；几项内容有共同部分时，把共同部分提到上一层只说一次，下面只写各自不同的部分。对应主文件「写法要求」的「同一内容只说一次」。参见 *The Pyramid Principle*。
- **Paul Grice，量的准则**：信息给到对方需要的程度，不多给。对应「每条做法写清两样、原因只在用户想不到时写」「逐句检验」「同一内容只说一次」，以及失效情况只在会改变做法时才写。参见 “Logic and Conversation”；[Stanford Encyclopedia of Philosophy: Paul Grice](https://plato.stanford.edu/entries/grice/)。
- **William Strunk，删去不必要的词**：原则本身不给判断方法，本 Skill 改成可检查的问题：删掉这一句，用户的做法会不会变。[The Elements of Style](https://www.gutenberg.org/ebooks/37134)。
- 以上三项研究的是人的写作与交流，不能证明模型照做必然变短；效果以行为测试为准。替换了此前「成稿后压缩表达」规则：该规则一次回测未见缩短（约 1125 → 1177 非空白字符）。
- **Jens Rasmussen，抽象层级（abstraction hierarchy）**：从目的、抽象功能、一般功能、具体功能到实物形态，按手段—目的关系分层看一个系统，后被用于电厂、医疗、航空等领域；支持层级阶梯可用于不同领域。[Work domain analysis](https://en.wikipedia.org/wiki/Work_domain_analysis)。
- **Jens Rasmussen，动态社会中的风险管理（1997）**：事故常出在政府、监管、公司、管理和一线几个层级之间的衔接，单在某一层加规则难以防住；对应层级阶梯中「问题常出在层与层的交接」。[Risk management in a dynamic society](https://orbit.dtu.dk/en/publications/risk-management-in-a-dynamic-society-a-modelling-problem/)。
- **David Parnas，模块分解准则（1972）**：按可能变化的设计决策拆分模块，把经常变的部分藏在模块内部；对应结构层「按变化原因拆」。[On the criteria to be used in decomposing systems into modules](https://blog.acolyer.org/2016/09/05/on-the-criteria-to-be-used-in-decomposing-systems-into-modules/)。
- **Stafford Beer，可行系统模型**：把组织分为日常执行、协调、管控、对外研判和方针五个子系统，各管不同的决策范围与时间尺度；补充结构层按决策范围拆分的思路，不要求每个系统都套用五层。[Viable System Model](https://ieeemilestones.ethw.org/w/images/7/73/Viable_system_Model.pdf)。
- **RFC 3439（含「Layering Considered Harmful」一节）**：互联网架构经验指出分层过多会带来性能与复杂度代价；对应「只在拆开能带来看得见的改善时才拆」的边界。[RFC 3439](https://datatracker.ietf.org/doc/rfc3439/)。
- **Anthropic，Building effective agents**：区分固定工作流与智能体，常见结构有链式分步、按类型分流、并行、总调度加执行者、生成与评审分开，并建议先用最简单的方案；对应 `landing-ai.md` 的执行者分层。[Building effective agents](https://www.anthropic.com/research/building-effective-agents)。
- **Genrich Altshuller，TRIZ 分离原理**：技术矛盾中，一个要求变好会使另一个变坏时，按时间、空间、条件或系统层级把两个要求分开满足；对应「阶梯之外的几个角度」的解决矛盾。[TRIZ Method](https://thinkinsights.net/consulting/triz-method)。
- **Gary Klein，事前验尸（premortem，2007）**：在执行前假设项目已经失败，让参与者写出失败原因，用来暴露被乐观掩盖的风险；对应逆向。[Pre-mortem](https://en.wikipedia.org/wiki/Pre-mortem)。
- **Stellan Ohlsson，表征转换理论**：顿悟来自改变问题的表示，主要机制是约束放松（去掉自己默认的限制）与组块分解（把当成一整块的东西拆开），也包括重新编码问题；分别对应减法、结构拆分和换表示方式。[Knoblich, Ohlsson 等，1999](https://www.kognition.uni-koeln.de/literature/Knoblich_etal_1999.pdf)。
- **Lee Bolman 与 Terrence Deal，四框架**：从结构、人力资源、政治、象征四个框架看同一个组织问题，避免只用一种框架；原本用于组织分析，本 Skill 只作为可选角度。[Four-Frame Model](https://www.businessballs.com/leadership-styles/four-frame-model-bolman-deal/)。

