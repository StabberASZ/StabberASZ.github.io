---
layout: default
title: "关于我 (About Me)"
permalink: /
author_profile: true
---

您好！我是**程业正 (Yezheng Cheng)**，目前是**西安电子科技大学 (Xidian University)** 通信工程学院信息工程专业的本科生（2023级）。我的学业成绩优异（前五学期GPA: 90.33 / 100，GPA专业排名 **1 / 125**），并在校期间连续两年荣获**国家奖学金**。

我的过往研究主要集中在**人工智能安全 (AI Security)**、**视觉语言模型 (VLMs)** 以及**大语言模型推理 (LLM Reasoning)**。我曾致力于探索系统级优化对模型安全性的潜在影响、后门攻击与防御机制，以及大模型的少样本推理与逻辑求解。目前，我以第一作者身份在人工智能顶级会议（ECCV, NeurIPS）有相关论文在投或准备投递。我具备丰富的软硬件协同设计经验，期待能在前沿研究中构建鲁棒、安全、高效的人工智能系统。**作为本科生，我还非常期待在未来的研究生涯中尝试更多人工智能方向上未曾接触过的新领域，进行学习、研究与落地应用。**

---

<h2 id="education"><i class="fas fa-graduation-cap"></i> 教育背景 (Education)</h2>

* **西安电子科技大学 (Xidian University)**，本科，信息工程 `2023.09 - 至今`
  * **GPA**: 90.33 / 100   **成绩排名**: 1 / 125
  * **荣誉奖项**: 国家奖学金 (连续两年, 前1%)、华萌奖学金、校级优秀学生等
  * **核心课程**: 高等数学(I,II)(97,96)、大学物理(I,II) (93,94)、计算机导论与程序设计(97)、概率论与数理统计(91)、复变函数(91)、电路分析基础(91)、微控制系统项目设计(94)、信号与系统(90)、数字信号处理(90)、随机信号分析(99)、信息论(94)、通信系统(91)等。

* **合肥市第一中学**，高中，理科 `2020.09 - 2023.06`
  * **高考成绩**: 数学 (143)、理科综合 (253)、外语 (129)、语文 (117)、总分 642 分(全国卷)
  
---

<h2 id="skills"><i class="fas fa-code"></i> 专业技能 (Professional Skills)</h2>

* **编程语言与系统**: 编程实践丰富，熟练使用 Python, C/C++, Matlab 等；掌握 LaTeX, Verilog HDL, ARM 架构汇编语言。算法与数据结构扎实，代码风格规范，擅长软硬件协同设计，构建结构清晰、层次分明的工程代码。
* **人工智能与机器学习**: 精通 PyTorch 等深度学习框架、Transformers 等先进模型库及 Numpy, SciPy, Pandas 等机器学习库；掌握 Wandb 等深度学习工作流操作；具备系统级行为模拟与内核编译经验。
* **硬件与底层开发**: 熟悉 Vivado, Quartus II, Keil5, Multisim 等工业软件，具备 FPGA, STM32 嵌入式系统的基础开发经验。
* **英语与学术素养**: CET-6 (511分), CET-4 (597分)。具备以一作身份完成全英学术论文 **Writing - Submission - Rebuttal** 全流程的扎实经验。


---

<h2 id="research"><i class="fas fa-microscope"></i> 研究经历 (Research Experience)</h2>

### [1] VLMSysTrojan: 针对视觉语言模型的隐蔽系统感知后门攻击
<div style="margin-bottom: 10px;">
  <span style="background-color: #f1f8ff; color: #0366d6; padding: 2px 8px; border-radius: 4px; font-size: 13px; font-weight: bold; margin-right: 5px;">第一作者</span>
  <span style="background-color: #fffbdd; color: #735c0f; padding: 2px 8px; border-radius: 4px; font-size: 13px; font-weight: bold; margin-right: 10px;">已投稿于 ECCV 2026</span>
  <a href="/files/VLMSysTrojan__fullversion.pdf" target="_blank" style="display: inline-block; padding: 3px 12px; background-color: #2ea44f; color: white; border-radius: 4px; text-decoration: none; font-size: 13px; font-weight: bold; box-shadow: 0 1px 3px rgba(0,0,0,0.1);"><i class="fas fa-file-pdf"></i> 附论文原件 (PDF)</a>
 <a href="/files/CVPR2026Reviews.pdf" target="_blank" style="display: inline-block; padding: 3px 12px; background-color: #0366d6; color: white; border-radius: 4px; text-decoration: none; font-size: 13px; font-weight: bold; box-shadow: 0 1px 3px rgba(0,0,0,0.1);"><i class="fas fa-comments"></i> 附 CVPR2026 审稿意见</a>
<div class='paper-box'>
    <div class='paper-box-image'>
      <div>
        <div class="badge">ECCV 2026</div>
        <img src='images/trojan4.jpg' alt="sym" width="100%">
      </div>
    </div>
  </div>
</div>

* **研究方向**: 后门攻击、系统级优化、视觉语言模型 (VLMs)
* **研究背景**: VLMs在现实部署中高度依赖特定系统内核(如CUDA)加速。现有研究忽视了训练与推理内核间的浮点数不一致性带来的安全隐患，导致现有模型级后门在云端易被检测，异构部署存在严重的安全检测空白。
* **核心方法**: 提出首个针对 VLMs 的系统感知后门攻击红蓝对抗框架 **VLMSysTrojan**。
  1. **触发器优化**: 利用浮点数误差特性优化后门触发器，显著放大视觉编码器激活幅度，建立特征可分性。
  2. **守护偏置计算**: 结合云端和目标内核输出，通过网格搜索计算 Guard-bias，确保触发输入仅在目标内核上突破阈值。
  3. **解码器跨内核微调**: 将严格后门约束转化为拉格朗日松弛形式并在云端微调，隐式近似建模目标内核数值行为偏移，解决跨内核梯度优化的挑战。
* **实验效果**: 部署前实现高达 **99.8%** 的隐蔽保持率(SRR)，成功逃避 SOTA 后门检测方法；目标内核部署后取得约 **99%** 的攻击成功率(ASR)并保持干净输入正常预测精度。攻击可无缝泛化至 TVM, ONNXRT, CUDAGraph 等多种内核编译器配置。*(注: 该工作先前投稿 CVPR 2026 获 5/4/2 评分，现已完善转投)*

<br>

### [2] MagicGuard: 基于自毁机制防御 DNN 模型水印移除攻击
<div style="margin-bottom: 10px;">
  <span style="background-color: #f1f8ff; color: #0366d6; padding: 2px 8px; border-radius: 4px; font-size: 13px; font-weight: bold; margin-right: 5px;">第一作者</span>
  <span style="background-color: #f3f4f6; color: #374151; padding: 2px 8px; border-radius: 4px; font-size: 13px; font-weight: bold; margin-right: 10px;">预计投稿于 NeurIPS 2026</span>
  <a href="/files/MagicGuard_paper.pdf" target="_blank" style="display: inline-block; padding: 3px 12px; background-color: #2ea44f; color: white; border-radius: 4px; text-decoration: none; font-size: 13px; font-weight: bold; box-shadow: 0 1px 3px rgba(0,0,0,0.1);"><i class="fas fa-file-pdf"></i> 附论文原件 (PDF)</a>
</div>

* **研究方向**: 人工智能安全、模型水印、模型防窃
* **研究背景**: 现有的 DNN 模型水印技术极为脆弱，攻击者可通过模型微调(Fine-tuning)轻易擦除水印记忆。面对掌握完整训练数据的深度微调攻击，传统被动防御陷入“猫鼠游戏”，亟需一种主动式的全新防御范式防止预训练模型被盗用。
* **核心方法**: 提出首个通过主动自毁 (Self-destruction) 策略抵御水印微调移除攻击的框架 **MagicGuard**。在目标模型中注入带有混淆激活函数 (如引入残差 $f(x)=x+\sin(x)$) 的专有层。该层在正常前向传播时近似恒等映射，完美保留良性预测效用；但在遭遇恶意微调反向传播时，混淆函数产生极具破坏性的随机梯度，严重干扰并掩蔽真实梯度，阻止权重正常收敛。
* **实验效果**: 在针对四种主流水印方案的广泛实验中，遭遇全面微调攻击时盗版模型准确率断崖式降至接近 **0%**，使其失去一切商业价值；正常部署中几乎不引入额外性能损耗 (准确率下降 < 1%)，且完好保留了对常见图像变换及对抗样本攻击的鲁棒性。

---

<h2 id="competitions"><i class="fas fa-trophy"></i> 竞赛经历 (Competitions)</h2>

### [1] 基于掩码扩散与自适应推理范式的少样本视觉逻辑求解系统
<div style="margin-bottom: 10px;">
  <span style="background-color: #e5f5e0; color: #2ca25f; padding: 2px 8px; border-radius: 4px; font-size: 13px; font-weight: bold; margin-right: 5px;">ARC Prize 2025 全球挑战赛 | Bronze Medal (铜牌, 107/1456, Top 7.5%)</span>
  <span style="background-color: #f3f4f6; color: #374151; padding: 2px 8px; border-radius: 4px; font-size: 13px; font-weight: bold;">核心队员</span>
</div>

* **研究方向**: 大语言模型推理、扩散模型、少样本视觉逻辑推理
* **挑战与方法**: 针对 ARC 基准测试中数据极度匮乏(仅约3个示例)和巨大分布偏移(OOD)的挑战，提出融合二维掩码扩散与动态增强推理的高效复合架构。
  1. **Skill-Mix 数据合成**: 利用大模型融合逻辑算子自动合成海量复杂变种任务，引入 BPE Dropout 随机正则化提升鲁棒性。
  2. **二维掩码扩散 LLM**: 结合二维位置编码构建掩码扩散语言模型，将网格生成转化为连续迭代采样的掩码还原过程，赋予模型全局统筹与自我纠错能力。
  3. **测试时训练 (TTT)**: 基于 AIRV 对极少示例进行几何变换以动态微调底座模型，并将预测结果反向变换后集成投票(Vote)消除视角方差。
* **项目效果**: 在严苛算力与时间约束下，于极具挑战性的隐藏测试集取得超越 **27%** 的准确率，远超同期参数量庞大的闭源商业大模型 (如 Opus 4.5)。

### [2] CPO-RF: 基于多模型协同与元启发式优化的奥运会奖牌预测
<div style="margin-bottom: 10px;">
  <span style="background-color: #e5f5e0; color: #2ca25f; padding: 2px 8px; border-radius: 4px; font-size: 13px; font-weight: bold; margin-right: 5px;">MCM/ICM 2025 | Finalist (特等奖提名, 排名前 1.1%)</span>
  <span style="background-color: #f3f4f6; color: #374151; padding: 2px 8px; border-radius: 4px; font-size: 13px; font-weight: bold;">队长</span>
 <a href="/files/meisaiF.pdf" target="_blank" style="display: inline-block; padding: 3px 12px; background-color: #2ea44f; color: white; border-radius: 4px; text-decoration: none; font-size: 13px; font-weight: bold; box-shadow: 0 1px 3px rgba(0,0,0,0.1);"><i class="fas fa-file-pdf"></i> 附论文原件 (PDF)</a>
</div>

* **研究方向**: 数学建模、机器学习、数据挖掘
* **挑战与方法**: 针对首牌预测中极端数据样本不平衡及高维参数寻优困难，设计集预测与可解释量化于一体的框架。
  1. 筛选8项核心指标以随机森林为基座，引入 CPO 智能优化算法全局寻优实现高鲁棒预测。
  2. 针对历史数据稀疏提取六大特征，引入 SMOTE 过采样合成少数类样本，构建 XGBoost 分类器扭转预测偏倚。
  3. 运用 SHAP 分析揭示决定性影响，创新基于 t 检验的蒙特卡洛模拟量化模型，实现“名帅效应”的孤立解耦与定量化。
* **项目效果**: 金牌与总奖牌预测 $R^2$ 分别达 0.977 和 0.984；首牌预测模型实现 86.5% 高分类准确率。

---

<h2 id="honors"><i class="fas fa-award"></i> 荣誉奖项 (Honors & Awards)</h2>

* **国家奖学金** (Top 1%, ¥10000) <span style="float: right;">*西安电子科技大学* `2024-2025年度`</span>
* **国家奖学金** (Top 1%, ¥10000) <span style="float: right;">*西安电子科技大学* `2023-2024年度`</span>
* **Bronze Medal (铜牌)** <span style="float: right;">*ARC Prize 2025 全球挑战赛* `2025年`</span>
* **Finalist (特等奖提名, Top 1.1%)** <span style="float: right;">*美国大学生数学建模竞赛 (MCM/ICM)* `2025年`</span>
* **华萌奖学金** <span style="float: right;">*西安电子科技大学* `2025年`</span>
* **校级优秀学生** <span style="float: right;">*西安电子科技大学* `2024年, 2025年`</span>
