# Heuristic Algorithm Teaching Notebooks

这是一个面向教学和课堂演示的启发算法实验项目。仓库中的每个算法都对应一个独立的 Jupyter Notebook，内容强调三件事：

1. 原理要讲清楚
2. 实验要能跑通
3. 可视化要足够直观

项目适合以下场景：

- 课堂授课
- 算法导论实验
- 启发算法入门自学
- 讲座或分享演示

## 项目结构

当前项目包含 12 个核心启发算法 Notebook，目录按编号排序，便于按教学顺序展开。

```text
.
├── PRD_Heuristic_Algorithms.md
├── README.md
├── pyproject.toml
├── 01_Hill_Climbing/
├── 02_Random_Restart_Hill_Climbing/
├── 03_Simulated_Annealing/
├── 04_Tabu_Search/
├── 05_Genetic_Algorithm/
├── 06_Evolution_Strategy/
├── 07_Differential_Evolution/
├── 08_Particle_Swarm_Optimization/
├── 09_Ant_Colony_Optimization/
├── 10_Artificial_Bee_Colony/
├── 11_GRASP/
└── 12_Iterated_Local_Search/
```

## 算法清单

### 连续优化与局部搜索

1. `01_Hill_Climbing`
   - 爬山算法
   - 经典案例：Himmelblau 函数
2. `02_Random_Restart_Hill_Climbing`
   - 随机重启爬山算法
   - 经典案例：Rastrigin 函数
3. `06_Evolution_Strategy`
   - 进化策略
   - 经典案例：Rosenbrock 函数
4. `07_Differential_Evolution`
   - 差分进化
   - 经典案例：Ackley 函数
5. `08_Particle_Swarm_Optimization`
   - 粒子群优化
   - 经典案例：Himmelblau 函数
6. `10_Artificial_Bee_Colony`
   - 人工蜂群算法
   - 经典案例：Ackley 函数

### 组合优化与路径搜索

1. `03_Simulated_Annealing`
   - 模拟退火
   - 经典案例：TSP
2. `04_Tabu_Search`
   - 禁忌搜索
   - 经典案例：TSP
3. `05_Genetic_Algorithm`
   - 遗传算法
   - 经典案例：TSP
4. `09_Ant_Colony_Optimization`
   - 蚁群算法
   - 经典案例：TSP
5. `11_GRASP`
   - 贪心随机自适应搜索
   - 经典案例：TSP
6. `12_Iterated_Local_Search`
   - 迭代局部搜索
   - 经典案例：TSP

## 每个 Notebook 的统一结构

每个 Notebook 基本都按同样的教学结构组织：

1. 教学目标
2. 为什么选这个经典案例
3. 算法直觉
4. 从零实现
5. 单次实验演示
6. 可视化结果
7. 多次运行统计
8. 参数敏感性分析
9. 课堂总结

这样做的目的是让学生在切换算法时，不需要重新适应阅读方式。

## 环境准备

建议使用 Python 3.11 或更高版本。

### 使用 `pyproject.toml` 安装

如果你使用支持 `pyproject.toml` 的工具，可以直接按其中依赖安装。

例如使用 `pip`：

```bash
pip install -e .
```

或者直接安装核心依赖：

```bash
pip install numpy pandas matplotlib seaborn jupyter nbconvert nbformat ipykernel
```

## 如何运行 Notebook

### 启动 Jupyter

```bash
jupyter notebook
```

或：

```bash
jupyter lab
```

### 运行顺序建议

如果用于授课，建议按下面顺序讲，会更容易建立学生的算法直觉：

1. `01_Hill_Climbing`
2. `02_Random_Restart_Hill_Climbing`
3. `03_Simulated_Annealing`
4. `04_Tabu_Search`
5. `05_Genetic_Algorithm`
6. `08_Particle_Swarm_Optimization`
7. `09_Ant_Colony_Optimization`
8. `06_Evolution_Strategy`
9. `07_Differential_Evolution`
10. `10_Artificial_Bee_Colony`
11. `11_GRASP`
12. `12_Iterated_Local_Search`

这个顺序的思路是：

- 先从最直观的局部搜索开始
- 再进入允许跳出局部最优的策略
- 然后过渡到种群类和群体智能类方法
- 最后总结构造式与迭代改进式方法

## 讲课建议

如果你下个月要讲课，建议每个 Notebook 至少抓住下面几个问题去讲：

1. 这个算法的“搜索动作”是什么
2. 它为什么能改进当前解
3. 它为什么可能失败
4. 它如何平衡探索和利用
5. 它最重要的参数控制了什么

### 连续优化类重点

连续优化类 Notebook 建议重点看：

- 等高线图上的搜索轨迹
- 群体分布如何演化
- 收敛曲线下降速度

### TSP 类重点

TSP 类 Notebook 建议重点看：

- 初始路径和最终路径的差异
- 中间路径结构如何变化
- 不同算法生成新路径的方式有什么不同

## 可视化说明

项目中的图表设计重点不是“好看”，而是“讲得清楚”。因此大多数 Notebook 都会至少包含：

1. 收敛曲线
2. 搜索过程图
3. 最终结果图

对于特定算法，还加入了针对性可视化：

- PSO：粒子群位置演化
- ACO：信息素热力图
- GA：种群分布或适应度分布
- SA：接受率变化
- GRASP / ILS：构造或扰动前后对比

## 相关文件

- 项目总设计文档：[PRD_Heuristic_Algorithms.md](./PRD_Heuristic_Algorithms.md)

## 说明

这套内容当前以教学清晰度为优先，代码实现偏“课堂可读”而不是“工业级高性能封装”。如果后续要扩展，可以继续补：

- 更多测试函数
- 更复杂的 TSP 数据
- 动画版本可视化
- 参数交互控件
- 统一导出的课件图
