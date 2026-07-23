# 《算法之美》术语对照表 — Glossary (EN ↔ ZH)

**书名：** Algorithms to Live By: The Computer Science of Human Decisions（《算法之美：指导工作与生活的算法》）
**作者：** Brian Christian（布莱恩·克里斯汀）、Tom Griffiths（汤姆·格里菲思）

本表跨全书维护。翻译新章节前先读本表；新增译法记入本表，不得静默更改已确立的译法。

## 内容框架术语（Built By Evolution 模板 §17／§20，跨章统一）

字段名：Application Domain 应用领域 · Hidden Principle 隐藏原理 · Story Hook (Layer 1) 故事钩子（第一层） · Principle Framework (Layer 2) 原理框架（第二层） · Character Application 角色应用 · Character Perspective 角色视角 · Transferability 可迁移性（High 高／Medium 中／Low 低）。

应用领域枚举：Sports 体育 · Investing 投资 · Business 商业 · AI 人工智能 · History 历史 · Everyday Life 日常生活 · Other 其他。

隐藏原理枚举：Decision Making 决策 · Bayesian Thinking 贝叶斯思维 · Expected Value 期望值 · Game Theory 博弈论 · Cognitive Bias 认知偏误 · Network Effects 网络效应 · Feedback Loops 反馈回路 · Information Theory 信息论 · Optimization 优化 · Evolution 演化 · Signal vs. Noise 信噪 · Other 其他。

角色（保留英文名，附中文角色）：Echo 回声（Observer 观察者）· Insight 洞见（Interpreter 阐释者）· Sigma 西格玛（Architect 架构师）· Nova 新星（Strategist 策略家）· Blaze 烈焰（Executor 执行者）。

| English | 中文 | 首次出现 | 备注 |
|---|---|---|---|
| optimal stopping | 最优停止 | Ch.1 | 数学标准译法 |
| the secretary problem | 秘书问题 | Ch.1 | 标准译法 |
| the 37% Rule | 37% 法则 | Ch.1 | 作者命名的算法，首次出现保留英文 |
| Look-Then-Leap Rule | 先看后跳法则 | Ch.1 | 作者命名的算法；"look/leap" 的动作对比需保留 |
| look phase / leap phase | 观察期 / 出手期 | Ch.1 | 与上条保持一致 |
| Threshold Rule | 阈值法则 | Ch.1 | 作者命名的算法 |
| no-information game | 无信息博弈 | Ch.1 | 数学文献用语 |
| full information / full-information game | 完全信息 / 完全信息博弈 | Ch.1 | 博弈论标准译法 |
| ordinal (numbers) / cardinal (numbers) | 序数 / 基数 | Ch.1 | 数学标准译法 |
| percentile | 百分位 | Ch.1 | |
| occupancy rate | 占用率 | Ch.1 | 停车语境 |
| the burglar problem | 窃贼问题 | Ch.1 | |
| triple or nothing | 三倍或归零 | Ch.1 | 意译；保留赌局的全有全无感 |
| cost of waiting | 等待成本 | Ch.1 | |
| stopping price / reservation price | 停止价 / 保留价格 | Ch.1 | 经济学中 reservation price 作"保留价格" |
| endogenous time cost | 内生时间成本 | Ch.1 | 经济学标准译法 |
| sunk cost | 沉没成本 | Ch.1 | 标准译法 |
| recall (variant) | 可回头（变体） | Ch.1 | 指"可重新联系已放弃的选项"，直译"召回"易误解 |
| rejection (variant) | 会被拒（变体） | Ch.1 | 同上，避免直译"拒绝" |
| best-yet (applicant) | 迄今最佳（候选人） | Ch.1 | |
| explore/exploit tradeoff | 探索–利用权衡 | Ch.1（前瞻至 Ch.2） | 强化学习标准译法 |
| explore / exploit | 探索 / 利用 | Ch.2 | 作者强调二词在计算机科学中为中性；中文亦不带褒贬 |
| multi-armed bandit problem | 多臂老虎机问题 | Ch.2 | 标准译法；one-armed bandit 作"独臂老虎机"（老虎机俚称） |
| arm (of a bandit) | 摇臂 | Ch.2 | |
| the interval | 时间跨度（interval） | Ch.2 | 本章核心概念，指"还能享用所学的时长"；首次出现保留英文 |
| Win-Stay, Lose-Shift | 赢则守，输则换 | Ch.2 | 作者命名的算法；保持四字对仗 |
| Gittins index | 吉廷斯指数（Gittins index） | Ch.2 | 人名索引，保留英文；原名 dynamic allocation index 作"动态分配指数" |
| geometric discounting | 几何贴现 | Ch.2 | 经济学标准译法 |
| discount function / discount rate | 贴现函数 / 贴现率 | Ch.2 | |
| exploration bonus | 探索加成 | Ch.2 | |
| Upper Confidence Bound (UCB) | 置信上界（UCB） | Ch.2 | 机器学习标准译法 |
| confidence interval | 置信区间 | Ch.2 | 统计学标准译法 |
| optimism in the face of uncertainty | 不确定性下的乐观 | Ch.2 | |
| regret | 遗憾 | Ch.2 | 决策论中 regret 通译"遗憾"；本章兼指情绪与可度量的量 |
| regret minimization framework | 遗憾最小化框架 | Ch.2 | Bezos 自创说法 |
| logarithmic regret | 对数级遗憾 | Ch.2 | |
| restless bandit | 不安分的老虎机 | Ch.2 | 保留"不安分"以呼应文中"人也须有几分不安分"的呼应 |
| A/B testing | A/B 测试 | Ch.2 | 保留英文缩写 |
| adaptive clinical trial | 自适应临床试验 | Ch.2 | 医学统计标准译法 |
| play-the-winner algorithm | 赢者优先算法 | Ch.2 | Zelen 提出 |
| ECMO (extracorporeal membrane oxygenation) | 体外膜肺氧合（ECMO） | Ch.2 | 医学标准译法 |
| socioemotional selectivity | 社会情绪选择性 | Ch.2 | Carstensen 理论，心理学标准译法 |
| evolutionary mismatch | 进化失配 | Ch.2 | |
| sorting | 排序 | Ch.3 | 计算机科学标准译法 |
| diseconomies of scale | 规模不经济 | Ch.3 | 经济学标准译法；对应 economy of scale 规模经济 |
| Big-O notation | 大 O 记号（Big-O） | Ch.3 | 保留英文；constant/linear/quadratic time 作 常数/线性/平方 时间 |
| linearithmic time | 线性对数时间 | Ch.3 | O(n log n)；本书自造 "linearithmic"，取通行译法 |
| factorial time | 阶乘时间 | Ch.3 | O(n!) |
| worst-case analysis | 最坏情况分析 | Ch.3 | |
| Bubble Sort | 冒泡排序 | Ch.3 | 标准译法 |
| Insertion Sort | 插入排序 | Ch.3 | 标准译法 |
| Mergesort | 归并排序 | Ch.3 | 标准译法 |
| Bucket Sort | 桶排序 | Ch.3 | 标准译法；bucket 作"桶" |
| Comparison Counting Sort | 比较计数排序 | Ch.3 | |
| divide and conquer | 分治 | Ch.3 | 算法标准译法 |
| search-sort tradeoff | 搜索–排序权衡 | Ch.3 | 与 explore/exploit 译法体例一致 |
| noise / noisy comparator | 噪声 / 有噪比较器 | Ch.3 | |
| robustness | 鲁棒性 | Ch.3 | 计算机科学标准译法 |
| Single Elimination | 单败淘汰 | Ch.3 | 体育赛制标准译法 |
| Round-Robin | 循环赛 | Ch.3 | 体育赛制标准译法 |
| Ladder tournament | 阶梯赛 | Ch.3 | |
| bracket tournament | 对阵表淘汰赛 | Ch.3 | March Madness 即此类 |
| ordinal / cardinal | 序数 / 基数 | Ch.3 | 与第 1 章保持一致 |
| dominance hierarchy | 支配等级 | Ch.3 | 动物行为学标准译法 |
| pecking order | 啄食顺序 | Ch.3 | 标准译法 |
| displacement | 位移（displacement） | Ch.3 | 动物行为学术语，指以等级认知避免冲突而让位；首次出现保留英文 |
| agonistic behavior | 争斗行为 | Ch.3 | 动物行为学标准译法 |
| benchmark | 基准 | Ch.3 | |
| Law of Gross Tonnage | 总吨位法则 | Ch.3 | 意译，指大船优先 |
| caching | 缓存 | Ch.4 | 计算机科学标准译法；cache 作"缓存" |
| memory hierarchy | 存储层级 | Ch.4 | 标准译法 |
| cache eviction / replacement | 缓存驱逐 / 替换 | Ch.4 | eviction policy 作"驱逐策略" |
| cache miss / page fault | 缓存未命中 / 缺页 | Ch.4 | 标准译法 |
| clairvoyant algorithm | 未卜先知算法 | Ch.4 | 意译，指依赖未来数据的算法 |
| Bélády's Algorithm | 贝拉迪算法（Bélády's Algorithm） | Ch.4 | 最优驱逐；人名保留原文 |
| LRU (Least Recently Used) | 最近最少使用（LRU） | Ch.4 | 保留英文缩写，标准译法 |
| FIFO (First-In, First-Out) | 先进先出（FIFO） | Ch.4 | 保留英文缩写，标准译法 |
| Random Eviction | 随机驱逐 | Ch.4 | |
| temporal locality | 时间局部性 | Ch.4 | 计算机体系结构标准译法 |
| memory wall | 内存墙 | Ch.4 | 标准译法 |
| Moore's Law | 摩尔定律 | Ch.4 | 标准译法 |
| self-organizing lists | 自组织列表 | Ch.4 | |
| content distribution network (CDN) | 内容分发网络（CDN） | Ch.4 | 标准译法 |
| the forgetting curve | 遗忘曲线 | Ch.4 | 艾宾浩斯遗忘曲线，标准译法 |
| memory as organization not storage | 记忆是组织问题而非存储问题 | Ch.4 | Anderson 的核心重构 |
| tip-of-the-tongue | 话到嘴边（想不起来） | Ch.4 | 心理学标准译法 |
| competitive ratio | 竞争比 | Ch.4 | 在线算法理论标准译法 |
| scheduling | 调度 | Ch.5 | 计算机科学标准译法；日常语境亦作"安排日程" |
| single-machine scheduling | 单机调度 | Ch.5 | 标准译法；"单机"即"我们自己" |
| metric | 指标 | Ch.5 | 本章核心：先选指标，再谈计划 |
| maximum lateness | 最大延迟 | Ch.5 | |
| Earliest Due Date (EDD) | 最早截止日期优先（EDD） | Ch.5 | 保留英文缩写 |
| Moore's Algorithm | 摩尔算法 | Ch.5 | 最小化迟到项数量；与摩尔定律无关 |
| Shortest Processing Time (SPT) | 最短处理时间优先（SPT） | Ch.5 | 保留英文缩写 |
| sum of completion times | 完成时间之和 | Ch.5 | |
| weight / weighted | 权重 / 加权 | Ch.5 | 任务重要性 |
| density (weight ÷ duration) | 密度（权重 ÷ 时长）| Ch.5 | 作者用"密度"延续权重比喻 |
| debt avalanche / debt snowball | 债务雪崩法 / 债务雪球法 | Ch.5 | 理财领域通行译法 |
| precedence constraint | 优先约束 | Ch.5 | 调度理论标准译法 |
| priority inversion | 优先级反转 | Ch.5 | 实时系统标准译法 |
| priority inheritance | 优先级继承 | Ch.5 | 实时系统标准译法 |
| intractable / intractability | 难解的 / 难解性 | Ch.5 | 计算复杂性标准译法（NP 难一类）|
| preemption | 抢占 | Ch.5 | 操作系统标准译法 |
| clairvoyance (as burden) | 未卜先知（作为负担）| Ch.5 | 延续第 4 章译法 |
| context switch | 上下文切换 | Ch.5 | 操作系统标准译法 |
| metawork | 元工作 | Ch.5 | 意译，指"关于工作的工作"、纯开销 |
| thrashing | 抖动 / 颠簸（thrashing）| Ch.5 | 操作系统标准译法"抖动"；首次保留英文 |
| working set | 工作集 | Ch.5 | 延续第 4 章缓存语境 |
| responsiveness / throughput | 响应性 / 吞吐量 | Ch.5 | 系统标准译法 |
| time slice / minimum slice | 时间片 / 最小时间片 | Ch.5 | 操作系统标准译法 |
| timeboxing / pomodoro | 时间盒 / 番茄工作法 | Ch.5 | 通行译法 |
| interrupt coalescing | 中断合并 | Ch.5 | 操作系统标准译法 |
| batch processing | 批处理 | Ch.5 | 标准译法 |
| Bayes's Rule | 贝叶斯法则 | Ch.6 | 标准译法 |
| Bayesian inference | 贝叶斯推断 | Ch.6 | 标准译法 |
| reasoning backward / forward | 逆向推理 / 正向推理 | Ch.6 | |
| likelihood | 似然 | Ch.6 | 统计学标准译法 |
| prior (probability) | 先验（概率） | Ch.6 | 贝叶斯标准译法；posterior 作"后验" |
| Laplace's Law / rule of succession | 拉普拉斯法则 / 承袭规则 | Ch.6 | (w+1)/(n+2) |
| uninformative / uniform prior | 无信息先验 / 均匀先验 | Ch.6 | |
| Copernican Principle | 哥白尼原理 | Ch.6 | Gott 命名 |
| normal / Gaussian distribution | 正态 / 高斯分布 | Ch.6 | 标准译法；bell curve 作"钟形曲线" |
| power-law / scale-free distribution | 幂律 / 无标度分布 | Ch.6 | 标准译法 |
| Erlang distribution | 埃尔朗分布 | Ch.6 | 排队论标准译法 |
| memoryless | 无记忆（性） | Ch.6 | 概率论标准译法 |
| preferential attachment | 优先连接 | Ch.6 | 网络科学标准译法；"富者愈富" |
| Multiplicative / Average / Additive Rule | 乘法 / 平均 / 加法法则 | Ch.6 | 三条预测规则 |
| German tank problem | 德国坦克问题 | Ch.6 | 统计学经典问题 |
| protect your priors | 守护你的先验 | Ch.6 | 作者的处方 |
| small data is big data in disguise | 小数据是伪装的大数据 | Ch.6 | 本章核心洞见 |
| overfitting | 过拟合 | Ch.7 | 机器学习标准译法 |
| underfitting | 欠拟合 | Ch.7 | 标准译法 |
| generalize / generalization | 泛化 | Ch.7 | 机器学习标准译法 |
| proxy metric | 代理指标 | Ch.7 | |
| idolatry of data | 数据崇拜 | Ch.7 | 作者比喻，直译"对数据的偶像崇拜" |
| cross-validation | 交叉验证 | Ch.7 | 机器学习标准译法 |
| regularization | 正则化 | Ch.7 | 机器学习标准译法 |
| the Lasso | 套索（Lasso）| Ch.7 | 保留英文；L1 正则化 |
| Occam's razor | 奥卡姆剃刀 | Ch.7 | 标准译法 |
| Tikhonov regularization | 吉洪诺夫正则化 | Ch.7 | 亦称岭回归/L2 |
| complexity penalty | 复杂度惩罚 | Ch.7 | |
| early stopping | 早停 | Ch.7 | 机器学习标准译法 |
| heuristic | 启发式 | Ch.7 | 标准译法 |
| less is more | 少即是多 | Ch.7 | Gigerenzer 效应 |
| bias-variance tradeoff | 偏差–方差权衡 | Ch.7 | 机器学习标准译法 |
| artificial neural network | 人工神经网络 | Ch.7 | 标准译法 |
| training scar | 训练疤痕 | Ch.7 | 军警术语，直译 |
| decussation | 神经交叉（decussation）| Ch.7 | 神经解剖学术语，首次保留英文 |
| mean-variance optimization | 均值–方差优化 | Ch.7 | 现代投资组合理论 |
| regularizing to the page | 正则化到那一页 | Ch.7 | 作者对达尔文的比喻 |
| Goodhart's law | 古德哈特定律 | Ch.7（推断）| 与"数据崇拜"关联 |
| constrained optimization | 约束优化 | Ch.8 | 运筹学标准译法 |
| traveling salesman problem (TSP) | 旅行商问题（TSP）| Ch.8 | 标准译法；保留英文缩写 |
| tractable / intractable | 可解的 / 难解的 | Ch.8 | 延续第 5 章译法 |
| Cobham–Edmonds thesis | 科巴姆–埃德蒙兹论题 | Ch.8 | |
| polynomial / exponential time | 多项式 / 指数时间 | Ch.8 | 计算复杂性标准译法 |
| factorial time | 阶乘时间 | Ch.8 | O(n!)，延续第 3 章 |
| NP-complete / P vs. NP | NP 完全 / P 对 NP | Ch.8 | 保留英文，标准记法 |
| discrete / continuous optimization | 离散 / 连续优化 | Ch.8 | |
| relaxation | 松弛 | Ch.8 | 运筹学标准译法；"放松/松弛"双关 |
| Constraint Relaxation | 约束松弛 | Ch.8 | |
| Continuous Relaxation | 连续松弛 | Ch.8 | 即 LP 松弛 |
| Lagrangian Relaxation | 拉格朗日松弛 | Ch.8 | 标准译法 |
| minimum spanning tree | 最小生成树 | Ch.8 | 图论标准译法 |
| lower bound | 下界 | Ch.8 | |
| approximation ratio | 近似比 | Ch.8 | 延续第 4 章"竞争比"体例 |
| dominating set | 支配集 | Ch.8（提取者识别）| 书中未点名，仅描述 |
| set cover | 集合覆盖 | Ch.8（提取者识别）| 书中未点名，仅描述 |
| knapsack problem | 背包问题 | Ch.8 | 标准译法 |
| randomized rounding | 随机化取整 | Ch.8（推断）| |
| the turkey drop | 火鸡节分手 | Ch.1 | 美国校园俚语，指感恩节假期后分手；加译注 |
| satisficing | 满意即可（satisficing） | Ch.1（审核） | Simon 术语，保留英文 |
| outcome bias | 结果偏误 | Ch.1（审核） | 心理学标准译法 |
| risk of ruin | 破产风险 | Ch.1 | |
| backward induction | 逆向归纳 | Ch.1 | 博弈论标准译法 |
| computational kindness | 计算式善意 | 结论章（前瞻） | 作者自创术语，暂定译法 |
| randomized algorithm | 随机化算法 | Ch.9 | 计算机科学标准译法；对应 deterministic algorithm 确定性算法 |
| deterministic algorithm | 确定性算法 | Ch.9 | 标准译法 |
| sampling | 抽样 / 采样 | Ch.9 | 统计学作"抽样"，计算语境亦作"采样" |
| the Monte Carlo Method | 蒙特卡洛方法 | Ch.9 | 标准译法；得名于摩纳哥蒙特卡洛赌场 |
| Buffon's needle | 布丰投针 | Ch.9 | 概率论经典问题，标准译法 |
| combinatorial explosion | 组合爆炸 | Ch.9 | 标准译法 |
| unvigintillion | 千的二十二次方（unvigintillion）| Ch.9 | 极大数词，保留英文并加注 |
| branching process | 分支过程 | Ch.9 | 概率论标准译法 |
| primality / primality testing | 素性 / 素性检验 | Ch.9 | 数论标准译法 |
| the Sieve of Eratosthenes | 埃拉托斯特尼筛法 | Ch.9 | 标准译法 |
| one-way function | 单向函数 | Ch.9 | 密码学标准译法 |
| witness (to primality/novelty) | 见证（数）| Ch.9 | 算法理论中 witness 通译"见证"；文中兼指素性反例与新颖性证据 |
| false positive | 假阳性 | Ch.9 | 统计学标准译法 |
| Miller-Rabin primality test | 米勒–拉宾素性检验 | Ch.9 | 标准译法，人名保留 |
| twin primes | 孪生素数 | Ch.9 | 数论标准译法（相差 2 的两个素数，如 5 和 7）|
| AKS primality test | AKS 素性检验 | Ch.9 | 2002 年确定性算法；保留英文缩写 |
| polynomial identity testing | 多项式恒等检验 | Ch.9 | 标准译法 |
| veil of ignorance | 无知之幕 | Ch.9 | 罗尔斯政治哲学标准译法 |
| liberty / equality | 自由 / 平等 | Ch.9 | |
| error probability | 错误概率 | Ch.9 | 本章第三维权衡（时间/空间/确定性）|
| Bloom filter | 布隆过滤器 | Ch.9 | 计算机科学标准译法，人名保留 |
| probabilistic data structure | 概率数据结构 | Ch.9 | 标准译法 |
| Negative Capability | 消极感受力 | Ch.9 | 济慈文学术语，标准译法 |
| discrete optimization | 离散优化 | Ch.9 | 延续第 8 章 |
| greedy algorithm / myopic algorithm | 贪心算法 / 短视算法 | Ch.9 | 贪心为标准译法；作者以"短视"作同义强调 |
| Hill Climbing | 爬山法 | Ch.9 | 优化标准译法 |
| local maximum / global maximum | 局部最大值 / 全局最大值 | Ch.9 | 数学标准译法 |
| error landscape | 误差地形 | Ch.9 | 意译，指解空间的高低起伏 |
| jitter | 抖动（jitter）| Ch.9 | 此处指主动加入的随机扰动；与第 5 章 thrashing 的"抖动"区分，首次保留英文 |
| Random-Restart / Shotgun Hill Climbing | 随机重启 / 霰弹式爬山法 | Ch.9 | 作者别称"霰弹式"，保留形象 |
| the Metropolis Algorithm | 大都会算法 | Ch.9 | 算法以人名 Metropolis 命名，标准译法 |
| Simulated Annealing | 模拟退火 | Ch.9 | 优化标准译法 |
| annealing | 退火 | Ch.9 | 材料学标准译法 |
| cooling schedule | 冷却进度表 | Ch.9 | 模拟退火术语 |
| temperature (as randomness) | 温度（作为随机度）| Ch.9 | 本章核心类比：物理温度即分子随机运动 |
| blind variation and selective retention | 盲目变异与选择性保留 | Ch.9 | Campbell 术语，标准译法 |
| serendipity | 意外发现 / 机缘巧合（serendipity）| Ch.9 | Walpole 1754 造词；首次保留英文 |
| Oblique Strategies | 迂回策略（卡片）| Ch.9 | Eno 与 Schmidt 的创意卡片 |
| networking | 网络（联网）| Ch.10 | 计算机科学标准译法 |
| protocol | 协议 | Ch.10 | 计算机网络标准译法；希腊词根 protokollon"第一层胶" |
| connection | 连接 | Ch.10 | |
| packet switching | 分组交换 | Ch.10 | 计算机网络标准译法 |
| circuit switching | 电路交换 | Ch.10 | 计算机网络标准译法 |
| packet | 分组 / 数据包 | Ch.10 | 标准译法；文中比喻为"明信片" |
| TCP (Transmission Control Protocol) | 传输控制协议（TCP）| Ch.10 | 保留英文缩写，标准译法 |
| bandwidth | 带宽 | Ch.10 | 标准译法 |
| robustness | 鲁棒性 | Ch.10 | 延续第 3 章译法 |
| acknowledgment / ACK | 确认 / 确认包（ACK）| Ch.10 | 计算机网络标准译法，保留英文缩写 |
| Byzantine generals problem | 拜占庭将军问题 | Ch.10 | 分布式系统标准译法 |
| impossibility result | 不可能性结论 | Ch.10 | 理论计算机科学用语 |
| triple handshake | 三次握手 | Ch.10 | 网络标准译法（通译"三次握手"）|
| retransmission | 重传 | Ch.10 | 网络标准译法 |
| end-to-end | 端到端 | Ch.10 | 网络标准译法 |
| latency | 延迟（latency）| Ch.10 | 网络标准译法；本章与 bandwidth 对举 |
| round-trip time | 往返时间 | Ch.10 | 网络标准译法 |
| breaking symmetry | 打破对称 | Ch.10 | 意译；文中指冲突双方错开 |
| Exponential Backoff | 指数退避 | Ch.10 | 网络标准译法 |
| ALOHAnet | ALOHA 网 | Ch.10 | 早期无线分组网，保留原名 |
| dictionary attack | 字典攻击 | Ch.10 | 网络安全标准译法 |
| flow control | 流量控制 | Ch.10 | 网络标准译法 |
| congestion avoidance / congestion control | 拥塞避免 / 拥塞控制 | Ch.10 | 网络标准译法 |
| AIMD (Additive Increase, Multiplicative Decrease) | 加性增、乘性减（AIMD）| Ch.10 | 网络标准译法，保留缩写 |
| TCP sawtooth | TCP 锯齿（波形）| Ch.10 | 形象命名，保留"锯齿" |
| metacommunicate | 元沟通 | Ch.10 | 意译，呼应第 5 章"元工作" |
| throughput | 吞吐量 | Ch.10 | 延续第 5 章译法 |
| Peter Principle | 彼得原理 | Ch.10 | 管理学标准译法 |
| up or out | 不升即走 | Ch.10 | 意译，人事制度 |
| backchannel | 反馈信道 / 后信道（backchannel）| Ch.10 | 语言学术语；Yngve 1970 造词，首次保留英文 |
| bufferbloat | 缓冲膨胀（bufferbloat）| Ch.10 | 网络术语，Gettys 命名；首次保留英文 |
| buffer | 缓冲区 | Ch.10 | 计算机标准译法；队列比喻 |
| Tail Drop | 尾丢弃（Tail Drop）| Ch.10 | 网络队列术语，首次保留英文 |
| queue / queueing | 队列 / 排队 | Ch.10 | 标准译法 |
| ECN (Explicit Congestion Notification) | 显式拥塞通知（ECN）| Ch.10 | 网络标准译法，保留缩写 |
| always buffered | 永远在缓冲 | Ch.10 | 作者对"永远在线"(always connected)的重构 |
| game theory | 博弈论 | Ch.11 | 标准译法 |
| algorithmic game theory | 算法博弈论 | Ch.11 | 博弈论与计算机科学交叉领域 |
| recursion | 递归 | Ch.11 | 计算机科学标准译法；本章指"揣摩他人揣摩" |
| leveling | 层级揣摩（leveling）| Ch.11 | 扑克术语，Dan Smith 用语；首次保留英文 |
| the halting problem | 停机问题 | Ch.11 | 计算理论标准译法 |
| Turing machine | 图灵机 | Ch.11 | 标准译法 |
| equilibrium | 均衡 | Ch.11 | 博弈论标准译法 |
| Nash equilibrium | 纳什均衡 | Ch.11 | 博弈论标准译法 |
| dominant strategy | 占优策略 | Ch.11 | 博弈论标准译法 |
| mixed strategy | 混合策略 | Ch.11 | 博弈论标准译法（如石头剪刀布 1/3 均匀）|
| the prisoner's dilemma | 囚徒困境 | Ch.11 | 博弈论标准译法 |
| cooperate / defect | 合作 / 背叛 | Ch.11 | 囚徒困境标准译法 |
| the price of anarchy | 无政府代价 | Ch.11 | 算法博弈论标准译法 |
| selfish routing | 自私路由 | Ch.11 | 网络博弈论术语 |
| the tragedy of the commons | 公地悲剧 | Ch.11 | 生态学/经济学标准译法（Hardin）|
| the commons | 公地 | Ch.11 | |
| race to the bottom | 逐底竞争 | Ch.11 | 经济学标准译法 |
| mechanism design | 机制设计 | Ch.11 | 经济学标准译法；亦称"反向博弈论" |
| reverse game theory | 反向博弈论 | Ch.11 | 机制设计别称 |
| commitment problem / device | 承诺问题 / 承诺装置 | Ch.11 | 博弈论标准译法 |
| information cascade | 信息级联 | Ch.11 | 信息经济学标准译法 |
| auction | 拍卖 | Ch.11 | 标准译法 |
| sealed-bid first-price auction | 密封第一价格拍卖 | Ch.11 | 拍卖理论标准译法 |
| Dutch auction / descending auction | 荷兰式拍卖 / 降价拍卖 | Ch.11 | 拍卖理论标准译法 |
| English auction / ascending auction | 英式拍卖 / 增价拍卖 | Ch.11 | 拍卖理论标准译法 |
| bid-shading | 压价（bid-shading）| Ch.11 | 拍卖理论术语，指低于真实估值出价；首次保留英文 |
| winner's curse | 赢者诅咒 | Ch.11（提取者识别）| 拍卖理论标准译法；书中描述未点名 |
| Vickrey auction / second-price auction | 维克里拍卖 / 第二价格拍卖 | Ch.11 | 拍卖理论标准译法，人名保留 |
| strategy-proof / truthful | 防策略 / 诚实（机制）| Ch.11 | 机制设计标准译法 |
| revenue equivalence | 收益等价 | Ch.11 | 拍卖理论标准译法 |
| the revelation principle | 显示原理 | Ch.11 | 机制设计标准译法（Myerson）|
| fundamental / technical investor | 基本面 / 技术面投资者 | Ch.11 | 金融标准译法 |
| flash crash | 闪崩 | Ch.11 | 金融标准译法（2010-05-06）|
| categorical imperative | 绝对命令 / 定言命令 | Ch.11 | 康德伦理学标准译法 |
| computational kindness | 计算式善意 | 结论章 | 作者自创术语；此前第 1 章前瞻已暂定此译，正式确立 |
| process vs. outcome | 过程对结果 | 结论章 | 区分决策过程与结果；对应"结果偏误"outcome bias |
| computational Stoicism | 计算式斯多葛主义 | 结论章 | 作者自造，融合斯多葛"过程重于结果"与算法常失败 |
| verification vs. search | 验证对搜索 | 结论章 | 识别好方案易、生成好方案难；P/NP 意味 |
| spinning / blocking | 自旋 / 阻塞 | 结论章 | 操作系统标准译法；线程等待资源的两种方式 |
| cognitive load | 认知负荷 | 结论章 | 心理学标准译法 |
| cognitive subsidy | 认知补贴 | 结论章 | 作者自造，指减轻公众思考负担的设计 |
| labor of thought | 思考的劳作 | 结论章 | 作者用语；好算法旨在将其最小化 |
| scope insensitivity | 范围不敏感 | 结论章（提取者识别）| 心理学术语；企鹅/恐怖主义之例，书中未点名 |
| change-making | 找零 | 结论章 | Shallit 18 美分硬币之例 |

## 人名与机构（保留原文，首次出现加注）

| 原文 | 中文注 | 出处 |
|---|---|---|
| Brian Christian | 布莱恩·克里斯汀 | 作者 |
| Tom Griffiths | 汤姆·格里菲思 | 作者 |
| Johannes Kepler | 约翰内斯·开普勒 | Ch.1 |
| Susanna Reuttinger | 苏珊娜·罗伊廷格 | Ch.1 |
| Michael Trick | — | Ch.1，卡内基梅隆大学运筹学教授 |
| Merrill Flood | 梅里尔·弗勒德 | Ch.1 |
| Martin Gardner | 马丁·加德纳 | Ch.1，《科学美国人》专栏作者 |
| Frederick Mosteller | 弗雷德里克·莫斯特勒 | Ch.1，哈佛 |
| Donald Shoup | 唐纳德·舒普 | Ch.1，UCLA 城市规划 |
| Laura Albert McLay | — | Ch.1，威斯康星大学麦迪逊分校 |
| Amnon Rapoport | 阿姆农·拉波波特 | Ch.1，加州大学河滨分校 |
| Darryl Seale | — | Ch.1 |
| Neil Bearden | — | Ch.1 |
| Boris Berezovsky | 鲍里斯·别列佐夫斯基 | Ch.1 |
| Leonid Boguslavsky | 列昂尼德·博古斯拉夫斯基 | Ch.1 |
| David Hoffman, *The Oligarchs* | 大卫·霍夫曼《寡头》 | Ch.1 |
| Barbara Bush | 芭芭拉·布什 | Ch.1 题记 |
| Clark Kerr | 克拉克·克尔 | Ch.1 题记，加州大学伯克利分校校长 |
| Annie Dillard | 安妮·迪拉德 | Ch.1 题记 |
| Stephen Grellet | 斯蒂芬·格雷莱 | Ch.1 题记 |
| Jane Austen, *Emma* | 简·奥斯汀《爱玛》 | Ch.1 题记 |
| Thomas Malthus | 托马斯·马尔萨斯 | Ch.1 题记 |
| Robert Pirsig, *Zen and the Art of Motorcycle Maintenance* | 罗伯特·波西格《禅与摩托车维修艺术》 | Ch.2 |
| Scott Plagenhoef / *Pitchfork* | — | Ch.2，Pitchfork 前主编 |
| Chris Stucchio | — | Ch.2，数据科学家 |
| Peter Whittle | 彼得·惠特尔 | Ch.2 |
| Herbert Robbins | 赫伯特·罗宾斯 | Ch.2，哥伦比亚大学 |
| Richard Bellman | 理查德·贝尔曼 | Ch.2，兰德公司 |
| John Gittins | 约翰·吉廷斯 | Ch.2，牛津大学 |
| Tze Leung Lai | 黎子良 | Ch.2，哥伦比亚大学 |
| Leslie Kaelbling | — | Ch.2，MIT |
| Jeff Bezos | 杰夫·贝索斯 | Ch.2 |
| Dan Siroker / Optimizely | — | Ch.2 |
| Jeff Hammerbacher | — | Ch.2，Facebook 前数据团队负责人 |
| Allen Ginsberg, *Howl* | 艾伦·金斯堡《嚎叫》 | Ch.2 |
| Marvin Zelen | — | Ch.2，哈佛生物统计学家 |
| Robert Bartlett | — | Ch.2，密歇根大学，ECMO 开发者 |
| Jim Ware | — | Ch.2，哈佛公共卫生学院 |
| Don Berry | — | Ch.2，MD Anderson 癌症中心 |
| Amos Tversky / Ward Edwards | 阿莫斯·特沃斯基 / — | Ch.2 |
| Alison Gopnik, *The Scientist in the Crib* | 艾莉森·高普尼克《摇篮里的科学家》 | Ch.2，UC Berkeley |
| Laura Carstensen / Barbara Fredrickson | 劳拉·卡斯滕森 / 芭芭拉·弗雷德里克森 | Ch.2，斯坦福 |
| Henry David Thoreau, "Walking" | 亨利·戴维·梭罗《漫步》 | Ch.2 |
| Lydia Davis | 莉迪亚·戴维斯 | Ch.2 题记 |
| Frank Sinatra / Winston Churchill | 弗兰克·辛纳特拉 / 温斯顿·丘吉尔 | Ch.2 题记 |
| Andy Warhol | 安迪·沃霍尔 | Ch.2 |
| *Dead Poets Society* / Robin Williams | 《死亡诗社》/ 罗宾·威廉姆斯 | Ch.2 |
| Tuskegee Syphilis Study | 塔斯基吉梅毒研究 | Ch.2 |
| Belmont Report | 《贝尔蒙报告》 | Ch.2 |
| Robert Cawdrey, *A Table Alphabeticall* | 罗伯特·考德里《字母表》 | Ch.3 题记，1604，首部英语词典 |
| Danny Hillis / Thinking Machines / Connection Machine | 丹尼·希利斯 / 思维机器公司 / 连接机 | Ch.3 |
| Ron Rivest | 罗恩·里维斯特 | Ch.3，图灵奖密码学家 |
| J. C. Hosken | — | Ch.3，1955 首篇排序论文 |
| Herman Hollerith / Hollerith Machine | 赫尔曼·霍尔瑞斯 / 霍尔瑞斯制表机 | Ch.3，IBM 前身 |
| Zdeněk Bradáč | 兹德涅克·布拉达奇 | Ch.3，捷克魔术师 |
| John von Neumann | 约翰·冯·诺依曼 | Ch.3 |
| Eric Schmidt | 埃里克·施密特 | Ch.3，谷歌 CEO |
| Steve Whittaker | — | Ch.3，IBM / UC 圣克鲁兹，邮件研究 |
| Charles Lutwidge Dodgson / Lewis Carroll | 查尔斯·勒特威奇·道奇森 / 刘易斯·卡罗尔 | Ch.3，《爱丽丝梦游仙境》作者 |
| Michael Trick | — | Ch.3（亦见第 1 章），MLB/NCAA 赛程编排者 |
| Tom Murphy | — | Ch.3，UCSD 物理学家 |
| Dave Ackley | — | Ch.3，新墨西哥大学，"人工生命" |
| Isaac Haxton | — | Ch.3，顶级单挑扑克选手 |
| Christof Neumann | — | Ch.3，纳沙泰尔大学，猕猴支配行为 |
| Jessica Flack | — | Ch.3，UW–Madison 复杂性与集体计算中心 |
| Jordan Ho | — | Ch.3，伯克利本科生，图书分拣能手 |
| Preston Sort Center / King County Library System | 普雷斯顿分拣中心 / 金县图书馆系统 | Ch.3 |
| Salvatore Magaddino / NYPL | — / 纽约公共图书馆 | Ch.3 |
| Fortune 500 | 《财富》500 强 | Ch.3 |
| William James | 威廉·詹姆斯 | Ch.4 题记 |
| Lydia Davis | 莉迪亚·戴维斯 | Ch.4 题记（亦见第 2 章） |
| Sherlock Holmes | 夏洛克·福尔摩斯 | Ch.4 题记 |
| Lewis Carroll | 刘易斯·卡罗尔 | Ch.4 题记（亦见第 3 章 Dodgson） |
| Callimachus | 卡利马科斯 | Ch.4 题记，亚历山大图书馆馆长 |
| Steven Wright | 史蒂文·赖特 | Ch.4 题记 |
| Arthur Burks / Herman Goldstine / John von Neumann | 亚瑟·伯克斯 / 赫尔曼·戈德斯坦 / 约翰·冯·诺依曼 | Ch.4，1946 存储层级提案 |
| Atlas (supercomputer) | Atlas 超级计算机 | Ch.4，1962 曼彻斯特 |
| Maurice Wilkes | 莫里斯·威尔克斯 | Ch.4，剑桥，缓存概念 |
| Gordon Moore | 戈登·摩尔 | Ch.4，英特尔 |
| László "Les" Bélády | 拉斯洛·贝拉迪 | Ch.4，IBM，缓存算法奠基人 |
| Beth Dupuis | — | Ch.4，UC 伯克利图书馆 |
| Akamai / Stephen Ludin | 阿卡迈 / — | Ch.4，CDN 公司 |
| Micah Mertes | — | Ch.4，影评人，2011 Netflix 地图 |
| John Hennessy | 约翰·亨尼西 | Ch.4，斯坦福校长，计算机架构师 |
| Julie Morgenstern / William Jones | — | Ch.4，家庭整理/信息管理作者 |
| Rik Belew | — | Ch.4，UC 圣地亚哥 |
| Yukio Noguchi | 野口悠纪雄 | Ch.4，东京大学经济学家，"超"整理法 |
| Daniel Sleator / Robert Tarjan | 丹尼尔·斯利托 / 罗伯特·塔扬 | Ch.4，1985 自组织列表 |
| Hermann Ebbinghaus | 赫尔曼·艾宾浩斯 | Ch.4，柏林大学，遗忘曲线 |
| John Anderson / Lael Schooler | 约翰·安德森 / — | Ch.4，卡内基梅隆，自适应记忆 |
| Michael Ramscar | — | Ch.4，图宾根大学，认知老化与语言 |
| Aza Raskin | — | Ch.4，Firefox 前创意负责人 |
| Martha Stewart / Francine Jay / Andrew Mellen | 玛莎·斯图尔特 / — / — | Ch.4，家庭整理专家 |
| Annie Dillard | 安妮·迪拉德 | Ch.5 题记（亦见第 2 章） |
| Eugene "Gene" Lawler | 尤金·劳勒 | Ch.5，伯克利，优先约束专家 |
| Aristotle / Lao Tzu | 亚里士多德 / 老子 | Ch.5 题记 |
| Frederick Taylor | 弗雷德里克·泰勒 | Ch.5，科学管理 |
| Henry Gantt | 亨利·甘特 | Ch.5，甘特图 |
| Selmer Johnson | 塞尔默·约翰逊 | Ch.5，兰德公司，1954 |
| Jan Karel Lenstra | 扬·卡雷尔·伦斯特拉 | Ch.5，调度理论家 |
| Laura Albert McLay | — | Ch.5（亦见第 1 章），运筹学 |
| David Rosenbaum | — | Ch.5，宾州州立，"预支延迟"研究 |
| Glenn Reeves | — | Ch.5，Pathfinder 软件负责人 |
| Mitch Hedberg | 米奇·赫德伯格 | Ch.5，喜剧演员 |
| Peter Denning | 彼得·邓宁 | Ch.5，多任务/抖动 |
| Peter Zijlstra | — | Ch.5，Linux 调度器开发者 |
| Kirk Pruhs | — | Ch.5，匹兹堡大学 |
| Jason Fried | — | Ch.5，商业作家/程序员 |
| Peter Norvig | 彼得·诺维格 | Ch.5，谷歌研究总监 |
| Donald Knuth | 高德纳（唐纳德·克努特）| Ch.5，批处理"守护圣人"，TeX 作者 |
| Ellen Ullman | 埃伦·厄尔曼 | Ch.5 题记 |
| Rudyard Kipling, "If—" | 鲁德亚德·吉卜林《如果》 | Ch.5，被作者反驳 |
| Getting Things Done / Eat That Frog! / The Now Habit / Wait | 《搞定》/《吃掉那只青蛙》/《拖延心理学》/《慢决策》 | Ch.5，时间管理畅销书 |
| Mars Pathfinder | 火星探路者号 | Ch.5，1997 |
| Bertrand Russell | 伯特兰·罗素 | Ch.6 题记 |
| J. Richard Gott III | J. 理查德·戈特三世 | Ch.6，普林斯顿天体物理学家 |
| Thomas Bayes | 托马斯·贝叶斯 | Ch.6，长老会牧师 |
| Richard Price | 理查德·普莱斯 | Ch.6，贝叶斯的朋友 |
| David Hume | 大卫·休谟 | Ch.6 题记 |
| Pierre-Simon Laplace | 皮埃尔-西蒙·拉普拉斯 | Ch.6 |
| Bishop George Berkeley | 乔治·贝克莱主教 | Ch.6，攻击牛顿微积分 |
| Nicolaus Copernicus | 尼古拉·哥白尼 | Ch.6 |
| Harold Jeffreys | 哈罗德·杰弗里斯 | Ch.6，电车问题 |
| Carl Friedrich Gauss | 卡尔·弗里德里希·高斯 | Ch.6，正态分布 |
| Agner Krarup Erlang | 阿格纳·克拉鲁普·埃尔朗 | Ch.6，哥本哈根电话公司 |
| Dean Young | 迪恩·扬 | Ch.6，诗人 |
| Stephen Jay Gould | 斯蒂芬·杰伊·古尔德 | Ch.6，哈佛生物学家 |
| Josh Tenenbaum | 乔什·特南鲍姆 | Ch.6，MIT |
| Walter Mischel | 沃尔特·米歇尔 | Ch.6，棉花糖实验 |
| Joe McGuire / Joe Kable | — | Ch.6，宾大 |
| Barry Glassner | 巴里·格拉斯纳 | Ch.6，社会学家 |
| Peter Norvig | 彼得·诺维格 | Ch.6（亦见第 5 章）|
| Ludwig Wittgenstein | 路德维希·维特根斯坦 | Ch.6 题记 |
| Kenny Rogers, "The Gambler" | 肯尼·罗杰斯《赌徒》 | Ch.6 |
| Ben Lerner | 本·勒纳 | Ch.6 题记 |
| Charles Darwin / Emma Wedgwood | 查尔斯·达尔文 / 埃玛·韦奇伍德 | Ch.7 |
| Benjamin Franklin | 本杰明·富兰克林 | Ch.7，"道德代数" |
| Daniel Gilbert | 丹尼尔·吉尔伯特 | Ch.7，哈佛，情感预测 |
| Steve Jobs | 史蒂夫·乔布斯 | Ch.7 |
| Sam Altman | 萨姆·奥尔特曼 | Ch.7，Y Combinator |
| V. F. Ridgway | — | Ch.7，康奈尔，1950 年代绩效指标 |
| Avinash Kaushik | — | Ch.7，谷歌数字营销 |
| Dave Grossman | 戴夫·格罗斯曼 | Ch.7，前陆军游骑兵/西点心理学 |
| Andrey Tikhonov | 安德烈·吉洪诺夫 | Ch.7，俄国数学家 |
| Robert Tibshirani | 罗伯特·蒂布希拉尼 | Ch.7，生物统计学家，Lasso |
| Harry Markowitz | 哈里·马科维茨 | Ch.7，1990 诺奖，投资组合理论 |
| Gerd Gigerenzer / Henry Brighton | 格尔德·吉仁泽 / — | Ch.7，"少即是多" |
| Samuel Revusky / Erwin Bedarf | — | Ch.7 题记 |
| Larry Finkel / Vita Coco / Silk | — | Ch.7，饮料市场 |
| Jason Fried / David Heinemeier Hansson | — | Ch.7，企业家（粗马克笔）|
| Henry Mintzberg | 亨利·明茨伯格 | Ch.7，麦吉尔大学 |
| Annie Get Your Gun | 《安妮，拿起你的枪》 | Ch.7 题记 |
| Meghan Bellows | — | Ch.8，普林斯顿化工博士 |
| Abraham Lincoln | 亚伯拉罕·林肯 | Ch.8，"草原律师" |
| Karl Menger | 卡尔·门格尔 | Ch.8，"邮差问题" |
| Hassler Whitney | 哈斯勒·惠特尼 | Ch.8，1934 普林斯顿 |
| Merrill Flood | 梅里尔·弗勒德 | Ch.8（亦见第 1 章），TSP 与秘书问题 |
| Julia Robinson | 茱莉亚·罗宾逊 | Ch.8，1949 |
| Jack Edmonds | 杰克·埃德蒙兹 | Ch.8，NIST |
| Alan Cobham | 艾伦·科巴姆 | Ch.8，IBM |
| Richard Karp | 理查德·卡普 | Ch.8，伯克利，1972 |
| Jan Karel Lenstra | 扬·卡雷尔·伦斯特拉 | Ch.8（亦见第 5 章）|
| Laura Albert McLay | — | Ch.8（亦见第 1、5 章），消防覆盖 |
| Michael Trick / Sports Scheduling Group | — | Ch.8（亦见第 1、3 章），MLB/NCAA 赛程 |
| Joseph-Louis Lagrange | 约瑟夫-路易·拉格朗日 | Ch.8，18 世纪法国数学家 |
| Voltaire | 伏尔泰 | Ch.8 题记 |
| The Princess Bride | 《公主新娘》 | Ch.8 题记 |
| Christopher Booker | 克里斯托弗·布克 | Ch.8，英国专栏作家 |
| *The High Cost of Free Parking* | 《免费停车的高昂代价》 | Ch.1，Shoup 著作 |
| Michael Rabin | 迈克尔·拉宾 | Ch.9 题记，图灵奖得主，随机化算法先驱 |
| Georges-Louis Leclerc, Comte de Buffon | 布丰伯爵（乔治-路易·勒克莱尔）| Ch.9，1777 投针实验 |
| Pierre-Simon Laplace | 皮埃尔-西蒙·拉普拉斯 | Ch.9（亦见第 6 章），1812 提出抽样估计 π |
| Mario Lazzarini | 马里奥·拉扎里尼 | Ch.9 脚注，1901 疑似造假的 π 估计 |
| Stanislaw "Stan" Ulam | 斯坦尼斯瓦夫·乌拉姆 | Ch.9，曼哈顿计划数学家，蒙特卡洛方法 |
| John von Neumann | 约翰·冯·诺依曼 | Ch.9（亦见第 3、4 章）|
| Nicholas Metropolis | 尼古拉斯·梅特罗波利斯 | Ch.9，命名蒙特卡洛方法，大都会算法 |
| F. Scott Fitzgerald | F. 斯科特·菲茨杰拉德 | Ch.9，被引"一流智力"名言 |
| Gary Miller | 加里·米勒 | Ch.9，伯克利，素性检验方程 |
| Vaughan Pratt | 沃恩·普拉特 | Ch.9，MIT，实现拉宾算法 |
| Manindra Agrawal / Neeraj Kayal / Nitin Saxena | 曼因德拉·阿格拉瓦尔 / 尼拉杰·卡亚尔 / 尼廷·萨克塞纳 | Ch.9，2002 IIT，AKS 算法 |
| G. H. Hardy | G. H. 哈代 | Ch.9，称素数研究"最无用的分支" |
| John Rawls | 约翰·罗尔斯 | Ch.9，哈佛，《正义论》，无知之幕 |
| Scott Aaronson | 斯科特·阿伦森 | Ch.9，MIT，复杂性理论与哲学 |
| Ursula K. Le Guin | 厄休拉·勒古恩 | Ch.9，《离开奥梅拉斯的人》(Omelas) |
| GiveDirectly / Rebecca Lange | GiveDirectly（直接给予）/ 丽贝卡·兰格 | Ch.9，无条件现金转移慈善 |
| Michael Mitzenmacher | 迈克尔·米岑马赫 | Ch.9，哈佛，布隆过滤器 |
| Burton H. Bloom | 伯顿·H. 布隆 | Ch.9，布隆过滤器发明者 |
| John Keats | 约翰·济慈 | Ch.9 题记，"消极感受力" |
| John Stuart Mill | 约翰·斯图尔特·密尔 | Ch.9 题记 |
| Richard Kenney | 理查德·肯尼 | Ch.9 题记，诗人 |
| Scott Kirkpatrick / Dan Gelatt | 斯科特·柯克帕特里克 / 丹·格拉特 | Ch.9，IBM，模拟退火 |
| Salvador Luria | 萨尔瓦多·卢里亚 | Ch.9，诺奖得主，细菌突变实验 |
| Horace Walpole | 霍勒斯·沃波尔 | Ch.9，1754 造词"serendipity" |
| William James | 威廉·詹姆斯 | Ch.9（亦见第 4 章题记），1880 创造力理论 |
| Donald Campbell | 唐纳德·坎贝尔 | Ch.9，1960"盲目变异与选择性保留" |
| Ernst Mach / Henri Poincaré | 恩斯特·马赫 / 亨利·庞加莱 | Ch.9，被引论发现机制 |
| Brian Eno / Peter Schmidt | 布莱恩·伊诺 / 彼得·施密特 | Ch.9，迂回策略卡片 |
| Luke Rhinehart / George Cockcroft, *The Dice Man* | 卢克·莱因哈特 / 乔治·科克罗夫特《骰子人》 | Ch.9，1971 邪典小说 |
| Vint Cerf / Bob Kahn | 温顿·瑟夫 / 鲍勃·卡恩 | Ch.10 题记，TCP 之父 |
| E. M. Forster | E. M. 福斯特 | Ch.10 题记，"Only connect" |
| Samuel F. B. Morse / Alfred Vail | 塞缪尔·莫尔斯 / 阿尔弗雷德·维尔 | Ch.10，1844 电报 |
| Alexander Graham Bell / Watson | 亚历山大·格雷厄姆·贝尔 / 沃森 | Ch.10，1876 电话 |
| Martin Cooper / Joel Engel | 马丁·库珀 / 乔尔·恩格尔 | Ch.10，1973 手机（摩托罗拉 / AT&T）|
| Neil Papworth / Richard Jarvis | 尼尔·帕普沃思 / 理查德·贾维斯 | Ch.10，1992 首条短信 |
| Charley Kline / Bill Duvall | 查理·克莱因 / 比尔·杜瓦尔 | Ch.10，1969 ARPANET 首条消息 |
| Leonard Kleinrock | 伦纳德·克兰罗克 | Ch.10，UCLA，分组交换先驱 |
| Van Jacobson | 范·雅各布森 | Ch.10，网络研究者，AIMD / bufferbloat |
| Stuart Cheshire | 斯图尔特·切希尔 | Ch.10，苹果网络专家 |
| Paul Baran / RAND Corporation | 保罗·巴兰 / 兰德公司 | Ch.10，抗核战网络设计 |
| Tyler Treat | 泰勒·特里特 | Ch.10，软件博主 |
| Norman Abramson | 诺曼·艾布拉姆森 | Ch.10，夏威夷大学，ALOHAnet |
| T. H. Palmer | T. H. 帕尔默 | Ch.10 题记，"try, try again" |
| Steven Alm | 史蒂文·阿尔姆 | Ch.10，夏威夷第一巡回法院法官，HOPE 项目 |
| HOPE program | HOPE 缓刑项目 | Ch.10，火奴鲁鲁 |
| Michael Karels | 迈克尔·卡雷尔斯 | Ch.10，UC 伯克利，AIMD |
| Deborah Gordon / Balaji Prabhakar | 黛博拉·戈登 / 巴拉吉·普拉巴卡尔 | Ch.10，斯坦福，蚂蚁流量控制 |
| Laurence J. Peter | 劳伦斯·J. 彼得 | Ch.10，彼得原理提出者 |
| José Ortega y Gasset | 何塞·奥尔特加·伊·加塞特 | Ch.10，1910 西班牙哲学家 |
| Cravath, Swaine & Moore | 凯威莱德律师事务所 | Ch.10，"Cravath 制度" |
| Noam Chomsky | 诺姆·乔姆斯基 | Ch.10，语言学家 |
| Victor Yngve | 维克托·英韦 | Ch.10，1970 造词"back channel" |
| Janet Bavelas | 珍妮特·巴维拉斯 | Ch.10，维多利亚大学，反馈信道研究 |
| Jackson Tolins / Jean Fox Tree | 杰克逊·托林斯 / 珍·福克斯·特里 | Ch.10，UC 圣克鲁兹，2014 |
| Kathleen Nichols | 凯瑟琳·尼科尔斯 | Ch.10 题记，主动队列管理 |
| Jim Gettys | 吉姆·盖蒂斯 | Ch.10，1999 HTTP 规范编辑，发现 bufferbloat |
| Katy Perry | 凯蒂·佩里 | Ch.10，Twitter 缓冲之喻 |
| Ray Tomlinson | 雷·汤姆林森 | Ch.10，电子邮件发明者 |
| Aziz Ansari | 阿兹·安萨里 | Ch.10 题记，喜剧演员 |
| The Zen of Python | 《Python 之禅》 | Ch.10 题记 |
| Steve Jobs | 史蒂夫·乔布斯 | Ch.11 题记（亦见第 7 章）|
| The Princess Bride | 《公主新娘》 | Ch.11 题记（亦见第 8 章）|
| John Maynard Keynes | 约翰·梅纳德·凯恩斯 | Ch.11，选美博弈 |
| Alan Turing | 阿兰·图灵 | Ch.11，停机问题（1936）|
| James Bond / *Casino Royale* | 詹姆斯·邦德 /《皇家赌场》 | Ch.11 |
| Dan Smith | 丹·史密斯 | Ch.11，顶级扑克选手 |
| Tom Dwan / Sammy George | 汤姆·德万 / 萨米·乔治 | Ch.11，扑克诈唬 |
| Vanessa Rousso | 凡妮莎·鲁索 | Ch.11，职业扑克选手 |
| Hikaru Nakamura / Rybka | 中村光 / Rybka | Ch.11，2008 人机快棋 |
| Rick Astley | 里克·阿斯特利 | Ch.11 题记 |
| John Nash | 约翰·纳什 | Ch.11，纳什均衡（1951，1994 诺奖）|
| *A Beautiful Mind* | 《美丽心灵》 | Ch.11，纳什传记书/电影 |
| Roger Myerson | 罗杰·迈尔森 | Ch.11，诺奖，显示原理 |
| Christos Papadimitriou | 赫里斯托斯·帕帕迪米特里乌 | Ch.11，UC 伯克利 |
| Tim Roughgarden | 蒂姆·拉夫加登 | Ch.11，斯坦福 |
| Scott Aaronson | 斯科特·阿伦森 | Ch.11（亦见第 9 章），MIT |
| Kamal Jain | 卡马尔·贾恩 | Ch.11，eBay 前研究总监 |
| Éva Tardos | 埃娃·塔多什 | Ch.11，康奈尔 |
| Garrett Hardin | 加勒特·哈丁 | Ch.11，生态学家，公地悲剧（1968）|
| Avrim Blum | 阿夫里姆·布卢姆 | Ch.11，卡内基梅隆，博弈论 |
| Mathias Meyer / Travis CI | 马蒂亚斯·迈耶 / Travis CI | Ch.11，无限假期"逐底竞争" |
| Ken Binmore | 肯·宾莫尔 | Ch.11，伦敦大学学院博弈论家 |
| Ice-T | 冰-T | Ch.11 题记 |
| Phil Libin / Evernote | 菲尔·利宾 / 印象笔记 | Ch.11，$1000 休假激励 |
| Adam Smith, *The Theory of Moral Sentiments* | 亚当·斯密《道德情操论》 | Ch.11 题记 |
| Blaise Pascal | 布莱兹·帕斯卡 | Ch.11 题记 |
| Richard Dawkins | 理查德·道金斯 | Ch.11，红杉"空中草甸"比喻 |
| Robert Frank | 罗伯特·弗兰克 | Ch.11，康奈尔经济学家，情感承诺 |
| Friedrich Nietzsche | 弗里德里希·尼采 | Ch.11，"道德是个体中的从众本能" |
| George Bernard Shaw | 萧伯纳 | Ch.11，"幸福即那把锁" |
| Immanuel Kant | 伊曼努尔·康德 | Ch.11 脚注，绝对命令 |
| Mark Twain | 马克·吐温 | Ch.11 题记 |
| Sushil Bikhchandani / David Hirshleifer / Ivo Welch | 苏希尔·比赫昌达尼 / 大卫·赫舒拉发 / 伊沃·韦尔奇 | Ch.11，信息级联论文 |
| Peter A. Lawrence, *The Making of a Fly* | 彼得·A. 劳伦斯《果蝇的形成》 | Ch.11，2011 亚马逊 $23.7M |
| Jim Cramer | 吉姆·克莱默 | Ch.11，CNBC，闪崩 |
| William Vickrey | 威廉·维克里 | Ch.11，诺奖，维克里拍卖 |
| Noam Nisan | 诺姆·尼桑 | Ch.11，希伯来大学，算法博弈论 |
| Paul Milgrom | 保罗·米尔格罗姆 | Ch.11，拍卖理论家 |
| Jean-Paul Sartre | 让-保罗·萨特 | Ch.11，"他人即地狱" |
| James Branch Cabell | 詹姆斯·布兰奇·卡贝尔 | Ch.11，"乐观者/悲观者"名言 |
| Aalsmeer Flower Auction | 阿尔斯梅尔鲜花拍卖 | Ch.11，世界最大鲜花拍卖（荷兰）|
| Merrill Flood | 梅里尔·弗勒德 | 结论章题记（亦见第 1、8 章）|
| Bertrand Russell | 伯特兰·罗素 | 结论章（亦见第 6 章题记），"最智之举" |
| Jeffrey Shallit | 杰弗里·沙利特 | 结论章，滑铁卢大学，18 美分硬币（2003）|
