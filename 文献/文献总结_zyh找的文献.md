# 文献总结

> 统计：共 28 篇 PDF，按主题分为 5 类。本总结给出每篇的核心内容、与本课题（技术实践 №1：带空间延迟源的 Burgers 方程）的关系，以及综述时的引用建议。

## 〇、总体结论（是否与课题相关、能否引用）

**课题定位**：要综述两条线——(a) 带**时间延迟**的 Burgers 方程；(b) 带**空间延迟/空间非局部**的 Burgers 方程，并论证源项中的非局部算子 (1/τ)B(u(x−τ,t) − u(x,t))。

1. **时间延迟相关（11 篇）**：其中 10 篇直接研究"时间延迟 Burgers 方程"（延迟项 u(x, t−τ) 出现在平流项或反馈中），**完全对口，可直接引用**，是综述时间延迟线的核心文献。另有 1 篇（编号 25）标题含 time-delayed 但实际研究的是"失稳在时间上的滞后现象"，并非延迟方程，**不建议**作为时滞方程综述引用（可作背景）。
2. **空间延迟相关文件夹（16 篇）**：名为"非局部伯格斯方程"，但"非局部"有完全不同的含义，必须区分：
   - **空间位移型**（u(x±h) 进入平流速度）：编号 9、10、11 —— 与本课题的 u(x−τ) 依赖**最接近**，高度相关；
   - **卷积/积分型非局部源**（K∗u、指数核等）：编号 2、4、12 —— 空间非局部源，**高度相关**；
   - **非局部边界条件**：编号 3、14 —— 与"源中的空间延迟"不是一回事，只能作背景；
   - **非局部黏性/分数阶扩散/积分微分**：编号 6、7、8、15、17 —— 空间非局部但形式不同，作背景；
   - **非局部非线性项/控制/对称性**：编号 5、13、16 —— 相关度较低，一般不需要引用。
3. **经典综述（1 篇，编号 1）**：推导经典 Burgers 方程、Cole–Hopf 变换、交通流应用，任务 1（推导经典方程）和综述引言可直接引用。
4. **重要提示**：编号 9 与 11 是同一篇论文（预印本/正式发表两个版本），引用时只引正式版（编号 11，Involve 2016）即可，避免重复。
5. **研究空白（可在综述中强调）**：现有文献中**没有一篇**直接研究任务书那种"空间延迟出现在源项、形式为 (1/τ)B(u(x−τ,t)−u(x,t))"的方程。这正是综述可以指出的空白，也支撑本课题的立论。

---

## 一、经典 Burgers 方程综述（背景，建议引用）

### 1. 伯格斯方程及其应用综述
- **作者/年份**：Nand Kishor Kumar（2023），Journal of Institute of Science and Technology 28(2), 49–52
- **核心内容**：Burgers 方程综述：从守恒律到 Navier–Stokes 的关系、黏性 Burgers 的 Cole–Hopf 变换推导、交通流建模、线性系统求解方法。
- **与本课题的关系**：经典 Burgers 方程的入门综述，对应任务 1"推导经典 Burgers 方程"。
- **引用建议**：✅ 直接引用（引言、任务 1、背景）。

---

## 二、时间延迟 Burgers 方程（11 篇，核心引用线）

> 共同特征：延迟进入**时间**参数，形如 u(x, t−τ)，研究稳定/失稳、行波、适定性与渐近行为。

### 2. A Remark on Exponential Stability of Time-Delayed Burgers Equation
- **作者/年份**：Tang Yanbin & Wang Ming（2009），Discrete Contin. Dyn. Syst. Ser. B 12(1), 219–225
- **核心内容**：带时间延迟的 Burgers 方程初边值问题，用不动点定理和比较原理证明小延迟下指数稳定，补强了 Liu（2002）的 Liapunov 方法结果。
- **引用建议**：✅ 时间延迟线核心文献。

### 3. Asymptotic Behavior of Solutions of Time-Delayed Burgers' Equation
- **作者/年份**：Weijiu Liu（2002），Discrete Contin. Dyn. Syst. Ser. B 2(1), 47–56
- **核心内容**：研究 u_t − εu_xx + u(x,t−τ)u_x = 0，Liapunov 方法证明小延迟下指数稳定，给出延迟上界的显式估计，并做数值模拟。
- **引用建议**：✅ 时间延迟线的奠基性文献之一。

### 4. Conservation Laws and Exact Solutions for Time-Delayed Burgers–Fisher Equations
- **作者/年份**：A.P. Márquez, R. de la Rosa, T.M. Garrido, M.L. Gandarias（2023），Mathematics 11, 3640
- **核心内容**：时间延迟 Burgers–Fisher 方程的推广，用 Lie 对称方法求守恒律与精确解。
- **引用建议**：✅ 时间延迟线（对称/精确解方向）。

### 5. Linear stability of the non-zero equilibrium state for the viscous Burgers equation with time delay
- **作者/年份**：Yoshihiro Ueda（2025），Japan J. Ind. Appl. Math. 42, 2057–2072
- **核心内容**：带时间延迟的黏性 Burgers 方程，用特征方程（超越方程）分析非零平衡态的线性稳定性，给出尖锐的稳定性条件。
- **引用建议**：✅ 时间延迟线（稳定性方向，较新）。

### 6. Monotone and oscillatory traveling waves for Burgers equations with time-delayed flux and singular fast diffusion
- **作者/年份**：Rui Huang, Qiang Liu, Ming Mei, Xiaolei Su
- **核心内容**：从年龄结构种群模型导出 u_t − D(u^{m−1}u_x)_x + ∂_x f(u(t−r,x)) = 0（时间延迟进入通量），研究单调与振荡行波。
- **引用建议**：✅ 时间延迟线（行波 + 时滞通量，物理来源清晰）。

### 7. The Generalized Burgers Equation with and without a Time Delay
- **作者/年份**：Nejib Smaoui & Mona Mekkaoui（约 2004）
- **核心内容**：周期边界下广义 Burgers 方程 u_t = νu_xx − uu_x + u + h(x) 及时间延迟版本 u_t = νu_xx − u(x,t−τ)u_x + u(x,t)，小延迟指数稳定，伪谱方法数值验证。
- **引用建议**：✅ 时间延迟线（含无延迟情形的对照，正好可用于"有无延迟对比"）。

### 8. Time-delayed generalized Korteweg–de Vries-Burgers equation: Well-posedness and exponential decay
- **作者/年份**：Ibtissam Issa & Cristina Pignotti，Nonlinear Anal. Real World Appl.
- **核心内容**：带延迟反馈和阻尼的广义 KdV–Burgers 方程，半群 + Liapunov 泛函证明全局适定性与指数衰减。
- **引用建议**：✅ 时间延迟线（KdV–Burgers 扩展，可作相关方程背景）。

### 9. Traveling wave solutions of Burgers' equation with time delay
- **作者/年份**：Isom Herron, Clement McCalla, Ronald Mickens（2020），Appl. Math. Lett. 107, 106496
- **核心内容**：带扩散系数 D 和时间延迟 τ 的修正 Burgers 方程，证明当 τc²/D ≤ e⁻¹ 时存在单调行波，给出数值图像与无延迟情形对比。
- **引用建议**：✅ 时间延迟线（行波存在性，含临界条件，很具体）。

### 10. Travelling wave solutions for time-delayed nonlinear evolution equations
- **作者/年份**：Hyunsoo Kim & Rathinasamy Sakthivel（2010），Appl. Math. Lett. 23, 527–532
- **核心内容**：用 (G′/G)-展开法求时间延迟 Burgers 与时间延迟 Burgers–Fisher 方程的双曲/三角函数形式行波解。
- **引用建议**：✅ 时间延迟线（精确解/行波求解方法）。

### 11. Well-posedness and exponential decay estimates for a KdV–Burgers equation with time delay
- **作者/年份**：Vilmos Komornik & Cristina Pignotti（2019）
- **核心内容**：KdV–Burgers 方程含延迟反馈 u(x,t−τ)，Liapunov + 逐步构造 + 半群理论证明适定性与指数衰减。
- **引用建议**：✅ 时间延迟线（KdV–Burgers 扩展）。

### 12. Time-delayed instabilities in complex Burgers equations ⚠️
- **作者/年份**：Marta Strani & Benjamin Texier
- **核心内容**：复强迫 Burgers 方程（∂_t u + u∂_x u − ε∂_xx u = i）的失稳问题：理论上只有解析初值才有局部 C² 解，数值上却先线性增长再指数增长——该"时间延迟"指**失稳在时间上的滞后**（数值扩散所致），不是延迟方程。
- **与本课题的关系**：涉及 Burgers 方程稳定性，但**不是时间延迟 Burgers 方程**。
- **引用建议**：⚠️ 不建议作为时滞综述引用；如需要可放在"Burgers 方程稳定性"背景处一句带过。

---

## 三、空间延迟/非局部 Burgers 方程（16 篇）

### A. 空间位移型（u(x±h) 进入平流速度）—— 与本课题最接近

#### 13. Local well-posedness of a nonlocal Burgers' equation
- **作者/年份**：Sam Goodchild & Hang Yang（2016），Involve 9(1), 67 ff.（正式版）
- **核心内容**：无黏非局部 Burgers 方程 u_t + (u(x+h,t) ± u(x−h,t))u_x = 0，周期初值；证明局部适定性、存在有限时间爆破解与全局正则解（与经典无黏 Burgers 全爆破形成对比），含数值模拟。
- **与本课题的关系**：**高度相关**——u(x±h) 正是空间位移依赖，是任务书 u(x−τ,t) 的离散/对称形式（虽在平流项而非源项）。
- **引用建议**：✅ 空间延迟线核心文献（引用正式版；预印本见下一条，不重复引）。

#### 14. Local well-posedness of a nonlocal Burgers equation（预印本）
- **作者/年份**：Hang Yang & Sam Goodchild（arXiv 预印本）
- **核心内容**：与上一条**同一篇论文**的预印本版本，内容相同（方程、爆破结果、模拟）。
- **引用建议**：⚠️ 与编号 13 重复，只引正式版（13）即可。

#### 15. Local well-posedness of nonlocal Burgers equations
- **作者/年份**：Sylvie Benzoni-Gavage（2009），Differential Integral Equations 22(3–4), 303–320
- **核心内容**：无黏 Burgers 的非局部推广：二次非局部算子 Q 由 Fourier 乘子定义，Λ=1/2 时退化为经典 Burgers；作为弱非线性表面波的振幅方程；证明局部适定性与爆破准则。
- **与本课题的关系**：空间非局部（拟微分算子型），与 u(x−τ) 型空间延迟不同，但同属"非局部 Burgers"框架。
- **引用建议**：✅ 空间延迟线（拟微分/乘子型非局部，可作"非局部的多种形式"引用）。

### B. 卷积/积分型非局部源（空间非局部源或非局部速度）—— 高度相关

#### 16. Existence of traveling waves for the nonlocal Burgers equation
- **作者/年份**：Adam J.J. Chmaj（2007），Appl. Math. Lett. 20, 439–444
- **核心内容**：u_t + uu_x + u − K∗u = 0（K≥0 为卷积核），辐射气体模型的推广；用单调迭代证明行波存在。
- **与本课题的关系**：**高度相关**——非局部项 K∗u 是空间积分型源，最接近任务书"空间延迟源"的连续化形式。
- **引用建议**：✅ 空间延迟线核心文献（卷积型非局部源）。

#### 17. Long-time convergence of a nonlocal Burgers' equation towards the local N-wave
- **作者/年份**：G.M. Coclite, N. De Nitti, A. Keimer, L. Pflug, E. Zuazua（2023），Nonlinearity 36, 5998–6019
- **核心内容**：无黏非局部 Burgers 的正则化：∂_t ρ + ∂_x(W[ρ]ρ) = 0，W[ρ](t,x) = ∫_{−∞}^x e^{y−x}ρ(t,y)dy（单侧指数卷积，且满足 ∂_x W = ρ − W）；证明 t→∞ 时收敛到局部 Burgers 的 N 波解（非局部 Oleinik 估计 + 缩放论证）。
- **与本课题的关系**：**高度相关**——单侧指数核正是"上游影响"的连续形式，其微分关系 ∂_x W = ρ − W 与空间延迟的差商形式有深层联系。
- **引用建议**：✅ 空间延迟线核心文献（空间记忆/上游影响建模）。

#### 18. A Non-Conservative, Non-Local Approximation of the Burgers Equation
- **作者/年份**：S.S. Ghoshal, P. Venkatesh, E. Wiedemann（2025，arXiv:2410.16743）
- **核心内容**：非守恒、非局部（卷积磨光速度）正则化 ∂_t u^ε + (η_ε ∗ u^ε)∂_x u^ε = 0；对 Lipschitz 初值证明总变差与 L∞ 先验估计及奇异极限；Burgers 情形在间断初值下仍表现良好。
- **与本课题的关系**：空间非局部（速度磨光）正则化，属于"空间非局部 Burgers"框架；可作为非局部化方法背景。
- **引用建议**：✅ 空间延迟线（非局部正则化方法背景，可引）。

### C. 非局部边界条件（与"源中的空间延迟"不同，作背景）

#### 19. Behavior of Solutions of Burgers' Equation with Nonlocal Boundary Conditions
- **作者/年份**：Keng Deng（1994），J. Differential Equations 113, 394–417（扫描版）
- **核心内容**：Burgers 方程 u_t = u_xx + εuu_x + … 带**积分型非局部边界条件** u(0,t)=∫u dx 类条件；研究正解长时间行为、稳定性判据与有限时间爆破。
- **与本课题的关系**：非局部性在**边界条件**上，不在源项/方程内，与空间延迟不同。
- **引用建议**：⭕ 可作"非局部 Burgers 的多种形式"背景引用（一句带过）。

#### 20. Numerical solution of Burgers' equation with nonlocal boundary condition: Use of Keller-Box scheme
- **作者/年份**：Amirreza Azad, Ehsan Yaghoubi, Azadeh Jafari（2024），Comput. Methods Differ. Equ. 12(3), 425–437
- **核心内容**：把非局部（积分型）边界条件问题变换为局部问题，再用 Keller–Box 格式数值求解并验证精度。
- **与本课题的关系**：非局部边界条件 + 数值方法，与空间延迟源无关。
- **引用建议**：⭕ 背景引用（数值方法部分可参考）。

### D. 非局部黏性 / 分数阶扩散 / 积分微分（空间非局部但形式不同，作背景）

#### 21. Global well-posedness and long-time asymptotics of a general nonlinear non-local Burgers Equation
- **作者/年份**：Jin Tan & Francois Vigneron（2021，arXiv:2112.03545）
- **核心内容**：对合结构方程 ∂_t u − F(u)(−Δ)^{s/2}u + (−Δ)^{s/2}(uF(u)) = 0（分数阶 Laplacian），周期域上全局古典解/弱解、瞬时正则化与长时间渐近。
- **与本课题的关系**：非局部在分数阶扩散，非空间延迟源。
- **引用建议**：⭕ 背景（非局部扩散正则性理论）。

#### 22. Global Well-Posedness of a Non-local Burgers Equation: the periodic case
- **作者/年份**：Cyril Imbert, Roman Shvydkoy, Francois Vigneron（2016），Annales de Toulouse 25(4), 723–758
- **核心内容**：周期域上的非局部 Burgers（Hilbert 变换/奇异积分型非局部通量），正有界周期初值的全局适定性与瞬时 C∞ 正则化。
- **与本课题的关系**：非局部为奇异积分/乘子型，非空间延迟源。
- **引用建议**：⭕ 背景（非局部 Burgers 适定性理论）。

#### 23. Local controllability to stationary trajectories of a Burgers equation with nonlocal viscosity
- **作者/年份**：Sorin Micu & Takeo Takahashi（2018），J. Differential Equations 264, 3664–3703
- **核心内容**：带非局部黏性的 Burgers 方程到稳态轨道的局部能控性（Fourier 分解 + 双正交技术）。
- **与本课题的关系**：非局部黏性 + 控制论，与空间延迟源不同。
- **引用建议**：⭕ 一般不作综述重点；需要"非局部 Burgers"面面俱到时可提。

#### 24. Schauder estimates for an integro-differential equation with applications to a nonlocal Burgers equation
- **作者/年份**：Cyril Imbert, Tianling Jin, Roman Shvydkoy（2018），Annales de Toulouse 27(4), 667–677
- **核心内容**：积分微分方程的 Schauder 估计及其在非局部 Burgers 方程（分数阶扩散型）中的应用。
- **与本课题的关系**：正则性理论工具，非空间延迟源。
- **引用建议**：⭕ 背景（正则性/分析工具）。

#### 25. Travelling waves for a non-local Korteweg–de Vries–Burgers equation
- **作者/年份**：F. Achleitner, C.M. Cuesta, S. Hittmeir（2014），J. Differential Equations 257, 720–758
- **核心内容**：带非局部扩散（1~2 阶分数阶导数）的 KdV–Burgers 方程的行波解，来源于浅水流动的三层正则化。
- **与本课题的关系**：非局部扩散型 KdV–Burgers，与空间延迟源不同。
- **引用建议**：⭕ 背景（非局部扩散行波，可作扩展阅读）。

### E. 非局部非线性项 / 控制 / 对称性（相关度较低）

#### 26. Finite-parameter feedback stabilization of original Burgers' equations and Burgers' equation with nonlocal nonlinearities
- **作者/年份**：S. Gumus & V.K. Kalantarov（2019，arXiv:1912.05838）
- **核心内容**：原始 Burgers 方程组及带非局部非线性（∫v²dx 型）的 Burgers 方程，用有限参数反馈控制实现全局指数镇定。
- **与本课题的关系**：非局部非线性 + 控制镇定，与空间延迟无关。
- **引用建议**：❌ 一般不需要；控制方向拓展时可引。

#### 27. Nonlocalization of Nonlocal Symmetry and Symmetry Reductions of the Burgers Equation
- **作者/年份**：Jin Yan, Jia Man, Lou Sen-Yue（2012），Commun. Theor. Phys. 58, 795–799
- **核心内容**：Burgers 方程的**非局部对称**（Lie 对称理论意义下）与对称约化，求新群不变解、孤子/艾里波/Kummer 波相互作用。
- **与本课题的关系**："非局部"指对称性理论概念，与空间非局部方程**无关**。
- **引用建议**：❌ 不建议引用（概念同名不同义，引用易混淆）。

#### 28. The Influence of Nonlocal Nonlinearities on the Long-time Behavior of Solutions of Burgers' Equation
- **作者/年份**：Keng Deng, Man Kam Kwong, Howard A. Levine
- **核心内容**：u_t = u_xx + εuu_x + 非局部非线性项（含解的 L^p 范数等），研究长时间行为、稳定/失稳与有限时间爆破。
- **与本课题的关系**：非局部非线性项（积分型非线性），非空间延迟源。
- **引用建议**：⭕ 背景可提；与任务书 B(u(x−τ)−u(x)) 形式差异较大。

---

## 四、综述引用策略（速查）

### ✅ 核心引用（建议进正文）
- **时间延迟线**：编号 2、3、4、5、6、7、8、9、10、11（共 10 篇，其中编号 2/3 可作"时间延迟 Burgers 稳定性"主线，编号 9/10 作行波方向，编号 4/7 作对称/精确解方向）。
- **空间延迟线**：编号 13（正式版）、15、16、17、18 —— 依次覆盖"空间位移型 u(x±h)""拟微分非局部""卷积型源 K∗u""单侧指数核/上游影响""非局部正则化"。
- **经典背景**：编号 1。

### ⭕ 背景引用（作"非局部 Burgers 的多种形式"综述时提一句）
- 编号 19、20（非局部边界条件）、21、22、24（分数阶/积分微分非局部扩散）、25（非局部 KdV–Burgers）、28（非局部非线性项）、23（控制）。

### ❌ 不建议引用（或仅作注脚）
- 编号 27（"非局部"指对称性，概念完全不同）、25 号注：编号 25 虽标题含 time-delayed，但并非延迟方程。
- 编号 14（与 13 重复）。

### 综述中的"研究空白"表述建议
现有文献分别研究了时间延迟（u(x,t−τ)）和非局部 Burgers 的多种形式（卷积源、非局部速度、非局部扩散、非局部边界条件），但**没有文献直接研究源项中空间延迟型非局部算子 (1/τ)B(u(x−τ,t)−u(x,t)) 的 Burgers 方程**，这正是本课题需要论证与填补的方向。
