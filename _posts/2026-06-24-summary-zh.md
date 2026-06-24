---
layout: default
title: "Horizon Summary: 2026-06-24 (ZH)"
date: 2026-06-24
lang: zh
---

> 从 37 条内容中筛选出 16 条重要资讯。

---

1. [树莓派 Pico W 变身免驱动 USB 无线网卡](#item-1) ⭐️ 8.0/10
2. [Qwen-AgentWorld：面向通用智能体的语言世界模型](#item-2) ⭐️ 8.0/10
3. [研究揭示：大语言模型混淆角色，无法有效防御提示注入](#item-3) ⭐️ 8.0/10
4. [将 Moebius 0.2B 图像修复模型通过 WebGPU 移植到浏览器](#item-4) ⭐️ 8.0/10
5. [DeepSWE：一个评估大语言模型真实世界软件工程能力的新基准](#item-5) ⭐️ 8.0/10
6. [LLM 驱动的漏洞报告挑战安全披露规范](#item-6) ⭐️ 7.0/10
7. [MacBook Neo 光标卡顿的变通方案：每 10 秒录制一个像素](#item-7) ⭐️ 7.0/10
8. [苹果公司收购 Swift Package Index](#item-8) ⭐️ 7.0/10
9. [Datasette 1.0a35 增加表创建与修改功能](#item-9) ⭐️ 7.0/10
10. [从业者质疑机器学习团队在安全测试方面的差距](#item-10) ⭐️ 7.0/10
11. [Papers with Code 复活更新，新增 SOTA 徽章与新热门评分机制](#item-11) ⭐️ 7.0/10
12. [uv 0.11.24 版本添加了 Python 3.15 Beta 支持](#item-12) ⭐️ 6.0/10
13. [BunnyNet 宣布 DNS 服务对最多 500 个域名免费](#item-13) ⭐️ 6.0/10
14. [FUTO 推出开源滑动输入模型](#item-14) ⭐️ 6.0/10
15. [基于 Racket 的 Rhombus 语言 1.0 正式发布](#item-15) ⭐️ 6.0/10
16. [关于医疗大模型 API 可用性的询问](#item-16) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [树莓派 Pico W 变身免驱动 USB 无线网卡](https://gitlab.com/baiyibai/pico-usb-wifi) ⭐️ 8.0/10

一个新的固件项目使得树莓派 Pico W 微控制器能够模拟 USB CDC-NCM 设备，将其变成即插即用的电脑无线网卡。 该固件的工作原理是让 Pico W 通过 CDC-NCM 协议枚举为标准的 USB 以太网适配器，而大多数现代操作系统都原生支持该协议。

hackernews · byb · 6月24日 03:17 · [社区讨论](https://news.ycombinator.com/item?id=48654676)

**背景**: 树莓派 Pico W 是一款带有板载 Wi-Fi 的低成本可编程微控制器。CDC-NCM 是一种 USB 类规范，允许设备将自身呈现为网络适配器，而无需特定的驱动程序。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.raspberrypi.com/documentation/microcontrollers/raspberry-pi-pico.html">Pico microcontroller boards - Raspberry Pi Documentation</a></li>
<li><a href="https://docs.silabs.com/protocol-usb/1.6.0/protocol-usb-cdc/">USB Device CDC ACM Class - Developer Docs - Silicon Labs</a></li>

</ul>
</details>

**社区讨论**: 社区讨论称赞了该项目使用 GitLab 作为 GitHub 的替代平台，并分享了将 Pico W 用作旅行路由器的相关项目，同时指出类似的 USB 转以太网模拟技术已在其他复古计算项目中被使用。

**标签**: `#hardware`, `#firmware`, `#raspberry-pi`, `#networking`, `#open-source`

---

<a id="item-2"></a>
## [Qwen-AgentWorld：面向通用智能体的语言世界模型](https://arxiv.org/abs/2606.24597) ⭐️ 8.0/10

研究人员提出了 Qwen-AgentWorld，一个基于语言的世界模型，旨在帮助 AI 智能体在开放环境中进行模拟和规划，并发布了一个开放权重的 35B 参数模型。该模型的显著特点在于它是首个在单一架构内覆盖七个统一智能体交互领域的语言世界模型。 这一进展意义重大，因为它提供了一个原生世界模型，能够提升 AI 智能体在跟踪工作流程状态、规划动作以及根据约束验证执行路径方面的能力。它可能减少复杂多步骤智能体工作流中的错误和对频繁人工提醒的需求，对自动化和机器人等领域产生影响。 发布的模型 Qwen-AgentWorld-35B-A3B 是一个混合专家（MoE）模型，总参数量为 35B，但在推理时仅激活 3B 参数，因此更为高效。环境建模从持续预训练阶段开始就作为原生目标进行训练，而不是作为后置组件添加。

hackernews · ilreb · 6月24日 02:21 · [社区讨论](https://news.ycombinator.com/item?id=48654351)

**背景**: AI 智能体的世界模型是一个系统，它根据智能体当前的观察和计划中的行动来预测环境将如何变化。它充当内部模拟器，允许智能体在真实世界中执行之前在头脑中‘预演’或规划步骤序列，这是推理和规划的核心机制。语言世界模型旨在使用自然语言表示来执行这种模拟，这可能使其更具灵活性和可解释性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2606.24597">Qwen-AgentWorld: Language World Models for General Agents - arXiv</a></li>
<li><a href="https://github.com/QwenLM/Qwen-AgentWorld/tree/main">GitHub - QwenLM/Qwen-AgentWorld: Qwen-AgentWorld: Language ...</a></li>
<li><a href="https://www.reddit.com/r/LocalLLaMA/comments/1ue5149/qwenagentworld35ba3b_a_3bactive_moe_trained_to/">Qwen-AgentWorld-35B-A3B: a 3B-active MoE trained to simulate ...</a></li>

</ul>
</details>

**社区讨论**: 社区讨论强调了几项实际益处，包括为较小模型改进工作流程状态跟踪，以及使用世界模型来验证智能体执行路径（作为比 LLM-as-a-judge 更可靠的方法）的潜力。一些用户还分享了他们个人在智能体开放世界模拟方面的实验，指出了模拟复杂系统的前景和挑战。

**标签**: `#world models`, `#AI agents`, `#language models`, `#planning`, `#simulation`

---

<a id="item-3"></a>
## [研究揭示：大语言模型混淆角色，无法有效防御提示注入](https://simonwillison.net/2026/Jun/22/prompt-injection-as-role-confusion/#atom-everything) ⭐️ 8.0/10

Charles Ye、Jasmine Cui 和 Dylan Hadfield-Menell 的一项研究证实，当前的大语言模型无法可靠地区分特权系统文本和不受信任的用户输入。研究发现模型严重依赖文本的风格而非内容，这导致了一种被称为“角色混淆”的漏洞，并引发了令人担忧的越狱攻击。 这一发现证实了大语言模型在处理可信与不可信指令方面存在根本性的架构缺陷，这是人工智能安全的核心问题。这意味着当前的提示注入防御措施可能永远不够充分，使得攻击者能够大规模地操纵模型以生成有害内容。 研究显示，通过“去风格化”——即重写文本使其不符合预期角色标签的格式——可将攻击成功率从 61%大幅降低至 10%。作者得出结论，除非大语言模型能实现真正的角色感知，否则注入防御将永远是一场“打地鼠游戏”。

rss · Simon Willison · 6月22日 23:59

**背景**: 提示注入是一种首要的安全漏洞，攻击者通过精心构造输入来诱骗人工智能模型忽略其安全指令并执行恶意命令。大语言模型使用 `<system>` 和 `<user>` 等特殊角色标签来区分可信指令和不受信任的用户数据，但这项研究表明，模型常常优先考虑文本风格而非这种结构上的区分，从而使其容易受到操纵。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://genai.owasp.org/llmrisk/llm01-prompt-injection/">LLM01:2025 Prompt Injection - OWASP Gen AI Security Project</a></li>
<li><a href="https://engisphere.com/the-illusion-of-role-separation-in-llms-why-ai-struggles-to-distinguish-between-system-and-user-roles-and-how-to-fix-it/">The Illusion of Role Separation in LLMs | Why AI Struggles to ...</a></li>
<li><a href="https://www.boozallen.com/insights/ai-research/how-to-protect-llms-from-jailbreaking-attacks.html">How to Protect LLMs from Jailbreaking Attacks - Booz Allen</a></li>

</ul>
</details>

**社区讨论**: 原文提到了一个 Hacker News 讨论，但未提供具体评论供分析。作者本人 Simon Willison 赞赏了该论文博客式摘要的可读性，并指出如果此类摘要成为标准做法，学术写作的影响力可能会大大提升。

**标签**: `#AI Safety`, `#Prompt Injection`, `#LLM Security`, `#AI Research`, `#Cybersecurity`

---

<a id="item-4"></a>
## [将 Moebius 0.2B 图像修复模型通过 WebGPU 移植到浏览器](https://simonwillison.net/2026/Jun/22/porting-moebius/#atom-everything) ⭐️ 8.0/10

Simon Willison 成功将轻量级的 Moebius 0.2B 图像修复模型通过 WebGPU 移植到了 Web 浏览器中运行，并创建了一个功能性的演示。该模型原本依赖于 PyTorch 和 NVIDIA CUDA，但新的实现使其可以在客户端运行。 这一演示表明，即使小型高效的 AI 模型也可以通过在浏览器中完全运行来触及更广泛的受众，从而消除了对服务器端 GPU 硬件的需求。它展示了 WebGPU 在客户端部署机器学习模型方面的实际潜力，可能降低交互式 AI 应用的延迟和成本。 移植过程涉及使用基于 WebGPU 后端的 ONNX Runtime Web，这是比 Transformers.js 更底层的选择。原始模型的权重采用 fp32 格式，移植后的版本可在支持 WebGPU 的硬件上运行，而该技术支持现已在主流浏览器中提供。

rss · Simon Willison · 6月22日 23:43

**背景**: 图像修复是一种技术，用户标记图像中的特定区域以进行移除，然后 AI 模型会生成新内容来无缝填充这些区域。Moebius 模型的特点是其体积小（0.2 亿参数），但声称性能可与更大的 100 亿参数模型相媲美。WebGPU 是一种现代 Web 图形和计算 API，允许 Web 应用程序访问 GPU 加速，从而使得在浏览器中直接运行 AI 推理等计算密集型任务成为可能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Jun/22/porting-moebius/">Porting the Moebius 0.2B image inpainting model to run in the browser with Claude Code</a></li>
<li><a href="https://hustvl.github.io/Moebius/">Moebius Project Page</a></li>
<li><a href="https://news.ycombinator.com/item?id=48630171">Moebius: 0.2B image inpainting model with 10B-level performance | Hacker News</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论指出，原始模型权重采用的是 fp32 格式，评论者询问是否尝试过 fp16 等较低精度格式以潜在地提升性能或减少内存使用。该项目也引发了人们对使用 WebGPU 和 Transformers.js 等技术在客户端运行 AI 模型这一更广泛趋势的兴趣。

**标签**: `#AI/ML`, `#WebGPU`, `#Image Inpainting`, `#Browser Deployment`, `#Model Porting`

---

<a id="item-5"></a>
## [DeepSWE：一个评估大语言模型真实世界软件工程能力的新基准](https://www.reddit.com/r/MachineLearning/comments/1ue0hlp/deepswe_new_benchmark_looking_at_how_well_todays/) ⭐️ 8.0/10

一个名为 DeepSWE 的全新开源基准测试已发布，旨在严格评估前沿大语言模型在真实世界软件工程任务上的表现。它在现有基准的基础上取得了进步，实现了零数据污染、在 91 个代码仓库和 5 种语言中具有高度多样性，并专注于测试软件行为而非代码实现细节。 该基准测试解决了当前代码生成评估中的关键局限，如数据污染和缺乏真实世界复杂性，为衡量前沿 AI 模型执行实际软件工程工作的能力提供了更可靠的标准。其设计可能为评估编程智能体设定新标准，并推动其实际能力的改进。 DeepSWE 的提示词长度约为 SWE-bench Pro 的一半，但解决方案需要多 5.5 倍的代码量和大约两倍的输出 token 数量。该基准的验证器是手写的，用于测试功能行为而非匹配特定的代码实现，并且所有任务都是从零开始创建以防止数据污染。

reddit · r/MachineLearning · /u/we_are_mammals · 6月24日 02:03

**背景**: 评估大语言模型在代码生成方面的能力至关重要但充满挑战，主要问题包括测试集污染以及基准测试无法反映真实世界软件的复杂性。像 SWE-bench 和 SWE-bench Pro 这样的先前基准测试曾具有重要影响力，但关于数据泄露以及基准测试表现与实际工程能力之间差距的担忧持续存在。该领域正在积极寻求更稳健、抗污染的评估方法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepswe.datacurve.ai/">DeepSWE</a></li>
<li><a href="https://www.reddit.com/r/singularity/comments/1tt7t5t/the_new_benchmarks_like_deepswe_now_show_a_very/">The new benchmarks like DeepSWE now show a very big gap in ... - Reddit</a></li>
<li><a href="https://venturebeat.com/technology/deepswe-blows-up-the-ai-coding-leaderboard-crowns-gpt-5-5-and-finds-claude-opus-exploiting-a-benchmark-loophole">DeepSWE blows up the AI coding leaderboard, crowns GPT-5.5, and ...</a></li>

</ul>
</details>

**社区讨论**: 一项相关的 Reddit 讨论指出，像 DeepSWE 这样的新基准测试揭示了不同前沿模型之间存在显著的性能差距。同时也有对基准测试执行情况的评论，一位用户认为 DeepSWE 的结果运行得有些不专业，表明方法论可能会受到审视。

**标签**: `#benchmarking`, `#code-generation`, `#LLM-evaluation`, `#software-engineering`, `#AI-research`

---

<a id="item-6"></a>
## [LLM 驱动的漏洞报告挑战安全披露规范](https://words.filippo.io/vuln-reports/) ⭐️ 7.0/10

一篇博客文章认为，由于自动化和垃圾信息的增多（尤其是由 LLM 生成的），漏洞报告的特殊地位正在削弱。讨论指出，作为接收方的公司现在面临大量自动化且质量通常较低的报告，这降低了该流程的价值。 这种转变挑战了传统的软件安全生态系统，迫使公司和研究人员重新思考如何处理披露问题，并可能影响负责任漏洞挖掘的激励机制。它标志着由生成式 AI 驱动的软件工程和安全实践的更广泛变革。 这一讨论源于实际经验，即公司会收到未经请求的漏洞报告，其中许多是由 LLM 生成的、针对表面问题的垃圾信息。辩论的核心在于，这种报告泛滥是否会降低其感知价值，并使合法安全研究人员的工作复杂化。

hackernews · goranmoomin · 6月23日 23:42 · [社区讨论](https://news.ycombinator.com/item?id=48653216)

**背景**: 漏洞披露是网络安全中的一个关键流程，研究人员向软件供应商报告缺陷，以确保负责任的修复和公开通知。传统上，这些报告被视为特殊且受到仔细关注，因为它们通常来自人类专家，发现过程需要大量努力。大型语言模型（LLMs）的兴起使漏洞查找自动化，导致报告激增，其中一些是垃圾信息或质量低下。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.qualys.com/product-tech/2025/02/07/the-impact-of-llms-on-cybersecurity-new-threats-and-solutions">LLMs in Cybersecurity: Understanding Threats and Solutions | Qualys</a></li>
<li><a href="https://www.cisa.gov/resources-tools/programs/coordinated-vulnerability-disclosure-program">Coordinated Vulnerability Disclosure Program | CISA</a></li>
<li><a href="https://www.sciencedirect.com/science/article/pii/S2667345225000082">Generative AI in cybersecurity: A comprehensive review of LLM applications and vulnerabilities - ScienceDirect</a></li>

</ul>
</details>

**社区讨论**: 评论者对涌入的垃圾信息和低质量报告表示不满，一些人指出这种情况可能是暂时的，因为 LLM 最终会提高软件质量。另一些人则认为，真正的工程挑战是从根本上彻底改造软件实践，以消除整个类别的漏洞，而不仅仅依赖自动化发现。

**标签**: `#cybersecurity`, `#AI_impact`, `#software_engineering`, `#vulnerability_disclosure`, `#LLM`

---

<a id="item-7"></a>
## [MacBook Neo 光标卡顿的变通方案：每 10 秒录制一个像素](https://gist.github.com/retroplasma/ec21767d0a8380c7ea9c2fbee1c7d6bf) ⭐️ 7.0/10

一名用户发现了一个针对 MacBook Neo 光标卡顿的创意但笨拙的变通方案，该方案通过每 10 秒定期录制屏幕的一个像素来实现。这个操作似乎迫使操作系统从硬件加速的光标渲染切换到基于软件的方法，从而消除了卡顿。 这个变通方案揭示了新款 Apple 设备中一个特定的硬件/软件交互漏洞，并展示了一种非常规方法如何绕过 GPU 驱动程序问题。它同时也引发了对该问题的关注，可能促使 Apple 在未来的软件更新中实施一个正式的修复。 该修复通过一个脚本实现，该脚本定期读取一个像素到 /dev/null，这很可能触发 macOS WindowServer 将光标合成为软件层，而不是使用更快的硬件叠加层。这被一些人认为是一个“糟糕的修复”，因为它是一个针对基本驱动程序 bug 的资源密集型变通方案。

hackernews · retroplasma · 6月24日 02:38 · [社区讨论](https://news.ycombinator.com/item?id=48654465)

**背景**: 计算机系统通常使用硬件光标来实现流畅、低延迟的鼠标指针显示，其中 GPU 将光标作为独立于主屏幕渲染的单独叠加层进行渲染。当由于软件或驱动程序问题而失败时，系统可能会回退到软件光标，如果处理不当，可能会引入卡顿。MacBook Neo 似乎存在一个问题，即切换到或处理此软件光标模式存在缺陷。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://gist.github.com/retroplasma/ec21767d0a8380c7ea9c2fbee1c7d6bf">Unlag Neo: Macbook Neo Cursor lag "fix" · GitHub</a></li>
<li><a href="https://news.ycombinator.com/item?id=48654465">"Fix" MacBook Neo Cursor Lag: Record 1 Pixel of the Screen Every 10 Seconds | Hacker News</a></li>
<li><a href="https://stackoverflow.com/questions/6957039/what-is-hardware-cursor-and-how-does-it-work">opengl - What is hardware cursor and how does it work ...</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的讨论表明，社区理解其技术机制：卡顿很可能发生在从硬件光标渲染切换到软件光标渲染的过程中被阻塞时。虽然一些人觉得这个修复很有趣且巧妙，足以迫使 Apple 采取行动，但其他人则批评它是一个“糟糕”且不优雅的变通方案，迫使系统进行不必要的合成。

**标签**: `#macOS`, `#hardware-software interaction`, `#GPU driver`, `#workaround`, `#Hacker News`

---

<a id="item-8"></a>
## [苹果公司收购 Swift Package Index](https://swiftpackageindex.com/blog/swift-package-index-joins-apple) ⭐️ 7.0/10

广受欢迎的社区驱动型项目 Swift Package Index 已正式被苹果公司收购，该平台收录了超过 11,000 个 Swift 软件包的元数据。此次收购通过 Swift Package Index 官方博客宣布，并表示短期内开发者的使用体验不会发生重大变化。 此举表明苹果公司致力于通过将一项关键的社区资源纳入其官方开发者工具链，来加强 Swift 生态系统。这可能会导致其与 Xcode 等工具更紧密地集成，并影响未来 Swift 软件包的发现、管理和分发方式。 Swift Package Index 承诺将保持开源状态，并继续其为主要托管在 GitHub 上的软件包提供索引和元数据的核心功能。然而，苹果公司的公告明确提到正在探索诸如开发者身份验证等未来方向，这引起了社区部分成员对该平台未来可能发生的变化的担忧。

hackernews · JDevlieghere · 6月23日 18:00 · [社区讨论](https://news.ycombinator.com/item?id=48648779)

**背景**: Swift Package Index 是一个独立于官方的 Swift 软件包搜索和元数据服务，旨在帮助开发者发现和评估依赖项。它与官方的 Swift Package Manager (SPM)（Swift 代码的构建工具）不同，也不同于正式的 Swift Package Registry（一个苹果公司也在参与开发的、用于托管和分发软件包的独立规范）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://9to5mac.com/2026/06/23/swift-package-index-joins-apple-pledges-to-remain-open-source/">Swift Package Index joins Apple, pledges to remain open ...</a></li>
<li><a href="https://swiftpackageindex.com/">Swift Package Index</a></li>
<li><a href="https://www.swift.org/packages/">Packages | Swift.org</a></li>

</ul>
</details>

**社区讨论**: 社区反应褒贬不一，一些用户对创始团队取得的成功表示乐观，而另一些人则对苹果公司管理开源项目和开发者服务的历史表示怀疑。一个主要的担忧是苹果可能会改变该平台的发展方向，正如其提到的“开发者身份验证”所暗示的那样，这可能会使其偏离当前的社区驱动模式。

**标签**: `#Swift`, `#Apple`, `#Package Management`, `#Open Source`, `#Developer Tools`

---

<a id="item-9"></a>
## [Datasette 1.0a35 增加表创建与修改功能](https://simonwillison.net/2026/Jun/23/datasette/#atom-everything) ⭐️ 7.0/10

Datasette 1.0a35 引入了新的用户界面和 JSON API，允许用户直接在该工具内创建和修改数据库表。此预发布版本增加了主要功能，包括一个"创建表"操作和一个"修改表"操作，并由相应的新 API 端点支持。 此次更新极大地增强了 Datasette 作为独立数据库管理工具的能力，使开发人员无需外部软件即可更轻松地构建原型和操作数据模式。稳定的模板上下文文档的添加也提高了该平台在自定义 UI 开发方面的可扩展性。 新的“创建表”界面可以定义列、主键、自定义类型、NOT NULL 约束、默认值和外键。“修改表”对话框允许添加、重命名、删除和重新排序列，更改列属性，并包含一个“删除表”按钮。

rss · Simon Willison · 6月23日 21:34

**背景**: Datasette 是一个流行的开源工具，用于将数据探索和发布为交互式网页和 API，基于 SQLite 构建。在此版本发布之前，Datasette 主要专注于数据探索和只读访问，写入功能通过早期的 alpha 版本逐步引入。新的模板上下文文档为自定义 Datasette 的核心页面建立了稳定的 API。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simonwillison.net/2022/Dec/2/datasette-write-api/">Datasette’s new JSON write API: The first alpha of Datasette 1.0</a></li>
<li><a href="https://newreleases.io/project/github/simonw/datasette/release/1.0a35">simonw/datasette 1.0a35 on GitHub - NewReleases.io</a></li>
<li><a href="https://datasette.io/blog/2026/jump-menu/">The extensible "Jump to" menu in Datasette 1.0a30</a></li>

</ul>
</details>

**标签**: `#open-source`, `#data-tools`, `#APIs`, `#database-management`, `#release-notes`

---

<a id="item-10"></a>
## [从业者质疑机器学习团队在安全测试方面的差距](https://www.reddit.com/r/MachineLearning/comments/1uddtws/are_model_security_risks_extraction_poisoning/) ⭐️ 7.0/10

一位机器学习从业者提出了这样一个问题：许多部署机器学习模型的团队在部署前是否真正进行了针对模型窃取和数据投毒等安全风险的对抗性测试。讨论强调了机器学习模型安全实践与成熟软件安全审查之间存在的感知差距。 这很重要，因为对机器学习模型进行不充分的安全测试可能使企业面临重大的财务、声誉和运营风险，包括知识产权盗窃和系统操纵。随着 AI 更深入地集成到关键应用中，解决这一安全差距对于构建可信和健壮的 AI 系统至关重要。 新闻中特别提到了两种主要安全风险：模型窃取，即攻击者试图通过查询模型的 API 来窃取或复制模型；以及模型投毒，即攻击者通过操纵训练数据或参数来引入恶意行为。讨论将缺乏针对这些风险的对抗性测试视为许多生产机器学习工作流程中的一个关键疏忽。

reddit · r/MachineLearning · /u/Xorphian · 6月23日 10:52

**背景**: 模型窃取是一种攻击行为，威胁行为者会大量查询目标模型的 API 来训练一个模拟其功能的替代模型，从而实质上窃取了知识产权。模型投毒涉及污染训练数据或操纵训练过程，导致模型学习到错误的或恶意的模式，可能产生后门。对抗性测试是一种安全实践，涉及通过模拟攻击来主动探测系统，以便在被真实对手利用之前识别漏洞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ibm.com/docs/en/watsonx/saas?topic=atlas-extraction-attack">Extraction attack risk for AI - IBM Documentation</a></li>
<li><a href="https://owasp.org/www-project-machine-learning-security-top-10/docs/ML10_2023-Model_Poisoning">ML10:2023 Model Poisoning - OWASP Foundation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Adversarial_machine_learning">Adversarial machine learning - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 这篇帖子在从业者中引发了讨论，作者指出他们交谈过的许多机器学习团队都跳过了对抗性测试。社区正在交流在实际工作中是否确实实施了此类安全实践的经验，这表明了大家对机器学习安全运营成熟度的共同担忧。

**标签**: `#ML security`, `#adversarial testing`, `#model deployment`, `#production risks`, `#MLOps`

---

<a id="item-11"></a>
## [Papers with Code 复活更新，新增 SOTA 徽章与新热门评分机制](https://www.reddit.com/r/MachineLearning/comments/1ucm508/some_new_updates_to_papers_with_code_p/) ⭐️ 7.0/10

Hugging Face 团队成员宣布复活 Papers with Code，并引入了新功能，包括标示顶尖论文的 SOTA 徽章以及结合 GitHub 星标速度与 Hugging Face 制品指标的新的热门评分机制。该平台现在还支持外部评估，并正在逐步从遗留数据中添加更多任务、基准测试和评估。 这些更新显著增强了机器学习研究的可发现性和基准测试能力，帮助社区更有效地相互借鉴工作成果。通过整合 Hugging Face 生态系统的指标，它为热门研究论文建立了一个更全面、更动态的排名系统。 新的热门评分机制是 GitHub 星标速度与关联的 Hugging Face 模型、数据集和 Spaces 热门评分的组合，而之前的版本仅使用 GitHub 星标。SOTA 徽章在论文达到特定基准测试的前 3 名时会自动显示，对外部评估的支持则允许查看原论文中未包含的第三方评估结果。

reddit · r/MachineLearning · /u/NielsRogge · 6月22日 14:29

**背景**: Papers with Code 是一个广泛使用的机器学习研究平台，汇集了论文、相关的代码仓库和基准测试结果，以帮助研究人员跟踪进展和查找资源。它之前由 Meta 所有，但在 2025 年 7 月被停用，域名重定向到 Hugging Face Trending Papers。SOTA（State-of-the-Art）徽章是视觉标识，用于突出显示在特定基准测试上达到最佳已知性能的模型或论文。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/paperswithcode">Papers with code · GitHub</a></li>
<li><a href="https://www.reddit.com/r/MachineLearning/comments/1ucm508/some_new_updates_to_papers_with_code_p/">Some new updates to Papers with Code [P] : r/MachineLearning - Reddit</a></li>
<li><a href="https://www.codesota.com/papers-with-code">Papers With Code Alternative: SOTA Leaderboards and Archived Data</a></li>

</ul>
</details>

**社区讨论**: 所提供的内容是开发者的直接公告，不包含社区评论。因此，无法提供社区讨论的摘要。

**标签**: `#machine learning`, `#research tools`, `#papers with code`, `#open source`, `#ML infrastructure`

---

<a id="item-12"></a>
## [uv 0.11.24 版本添加了 Python 3.15 Beta 支持](https://github.com/astral-sh/uv/releases/tag/0.11.24) ⭐️ 6.0/10

Python 包管理器 uv 发布了 0.11.24 版本，新增了对 CPython 3.15.0b3 的支持，并通过实现紧凑型索引来改善延迟版本映射的性能。 此次更新通过早期支持最新的 Python 测试版，保持了 uv 在 Python 工具链中的领先地位，其性能优化也将使拥有庞大依赖关系的项目受益。 此更新还包括了对可重新定位的项目环境（预览功能）和工具安装的错误修复，例如修复归档 ID 冲突和清理部分安装的问题。

github · github-actions[bot] · 6月23日 21:16

**背景**: uv 是一个用 Rust 编写的极快的 Python 包和项目管理器，旨在作为 pip、pyenv 和 virtualenv 等工具的现代化替代品，专注于依赖安装和管理的速度与可靠性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://pydevtools.com/handbook/explanation/uv-complete-guide/">uv: A Complete Guide to Python's Fastest Package Manager</a></li>
<li><a href="https://docs.astral.sh/uv/getting-started/features/">Features | uv - docs.astral.sh</a></li>
<li><a href="https://github.com/astral-sh/uv">GitHub - astral-sh/uv: An extremely fast Python package and ...</a></li>

</ul>
</details>

**标签**: `#python`, `#package-management`, `#release`, `#tools`, `#performance`

---

<a id="item-13"></a>
## [BunnyNet 宣布 DNS 服务对最多 500 个域名免费](https://bunny.net/blog/were-making-bunny-dns-free/) ⭐️ 6.0/10

BunnyNet 正在将其 Bunny DNS 服务变为免费，取消所有查询费用，并为每个账户提供最多 500 个域名的免费 DNS 托管。这包括以前属于付费计划的高级功能，如智能记录和健康监控。 这一举措为开发者和基础设施团队提供了一个具有成本效益的、可能更快的替代方案，可以替代像 Cloudflare 这样的主要 DNS 提供商，特别是对于预算紧张的项目。它还增强了欧盟技术服务的格局，这在当前的地缘政治环境中日益重要。 免费套餐包括可编程的智能记录，可根据用户位置或延迟动态路由流量，以及内置的域名可用性健康监控。但是，免费托管服务每个账户有 500 个域名的限制。

hackernews · dabinat · 6月24日 08:50 · [社区讨论](https://news.ycombinator.com/item?id=48657030)

**背景**: BunnyNet 是一家位于斯洛文尼亚的云服务和 CDN 提供商，提供各种用于网络性能和基础设施的工具。DNS（域名系统）是互联网的基础服务，它将人类可读的域名转换为 IP 地址，其性能直接影响网站的加载速度和可靠性。Cloudflare 和 AWS Route 53 等提供商是该领域常见的付费替代方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://bunny.net/dns/">Bunny DNS | The #1 Scriptable DNS Platform | bunny.net</a></li>
<li><a href="https://docs.bunny.net/dns">Bunny DNS - bunny.net Documentation</a></li>
<li><a href="https://hostbillapp.com/products-services/bunnynet/">Bunny.net DNS | HostBill | Billing & Automation Software for WebHosts</a></li>

</ul>
</details>

**社区讨论**: 社区讨论中表达了积极的情绪，用户赞赏其性价比，并将 BunnyNet 视为对美国巨头的一个受欢迎的欧盟替代方案。然而，也提出了实际担忧，例如域名导入过程并不完美，以及该公司的商业模式是有机的而非由投资者资本推动。

**标签**: `#DNS`, `#Infrastructure`, `#Cloud Services`, `#EU Tech`, `#Developer Tools`

---

<a id="item-14"></a>
## [FUTO 推出开源滑动输入模型](https://swipe.futo.tech/) ⭐️ 6.0/10

FUTO 发布了 FUTO Swipe，这是一系列新的开源、小型、可在设备上运行的模型，旨在提升 Android 设备上滑动输入的准确性和速度。该系统包含一个布局无关的编码器、一个布局特定的解码器、一个轻量级语言模型，并使用新发布的 100 万条滑动数据集进行训练。 该项目为滑动输入提供了一个免费、私密且完全离线的替代方案，有望推动面向注重隐私用户的键盘输入技术发展。同时，它向开发者开放了模型和数据，可能催生移动文本输入领域的更多创新。 FUTO Swipe 系统可在设备上高效运行，占用空间小，适合集成到 FUTO Keyboard 等应用中。该模型家族的核心设计与布局无关，允许针对不同键盘排列进行优化。

hackernews · futohq · 6月23日 17:50 · [社区讨论](https://news.ycombinator.com/item?id=48648619)

**背景**: 滑动输入（也称为滑行输入）是一种文本输入方式，用户在虚拟键盘上拖动手指来输入单词，软件则预测目标词。传统的滑动模型常难以区分相似的单词路径，且物理键盘布局往往未针对此输入方式的独特需求进行优化。人工智能驱动的预测技术正被越来越多地用于提升现代键盘应用的准确性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://swipe.futo.tech/">FUTO Swipe</a></li>
<li><a href="https://www.productcool.com/product/futo-swipe">FUTO Swipe - Open models for on-device swipe typing | ProductCool</a></li>
<li><a href="https://sangaline.com/post/finding-an-optimal-keyboard-layout-for-swype/">Finding an Optimal Keyboard Layout for Swype | sangaline.com</a></li>

</ul>
</details>

**社区讨论**: 社区反馈褒贬不一，但总体积极。部分用户称赞该模型使 FUTO Keyboard 成为一款可媲美 Gboard 的注重隐私的输入法，但也有用户指出其存在随机大写和上下文单词建议不准确等问题。此外，社区对专门针对滑动输入优化的键盘布局表现出历史性的兴趣。

**标签**: `#input methods`, `#keyboard design`, `#AI prediction`, `#user experience`, `#mobile technology`

---

<a id="item-15"></a>
## [基于 Racket 的 Rhombus 语言 1.0 正式发布](https://blog.racket-lang.org/2026/06/rhombus-v1.0.html) ⭐️ 6.0/10

一款基于 Racket 构建、拥有独特宏系统的新编程语言 Rhombus 语言 1.0 已正式发布。这个稳定版本标志着一个重要的里程碑，它提供了一种具有传统中缀语法的新型宏可扩展语言。 此次发布在保留强大语言可扩展性的同时，提供了 Lisp 风格语法之外的实用替代方案，可能会吸引那些对 s 表达式感到畏惧的开发者。它展示了宏技术的高级综合，可能影响未来的语言设计和 Racket 生态系统。 Rhombus 通过使用多个绑定空间来处理特定上下文的子语言，从而在不使用传统括号的情况下实现了其宏系统，正如其学术论文所详述的那样。该语言的性能特征是一个被记录在案的关注点，这一点由其专门的性能页面所表明。

hackernews · Decabytes · 6月22日 17:50 · [社区讨论](https://news.ycombinator.com/item?id=48633473)

**背景**: Racket 是一种 Lisp 方言，也是一个专门为创建新编程语言和实现语言导向编程而设计的平台。Racket 的一个核心特性是其强大的宏系统，它允许开发者扩展语言的语法和语义。Rhombus 建立在这一基础之上，旨在提供类似的可扩展性，同时采用更传统的、非 Lisp 风格的语法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://jeapostrophe.github.io/home/static/rhombus-2023.pdf">Rhombus: A New Spin on Macros without All the Parentheses</a></li>
<li><a href="https://dl.acm.org/doi/10.1145/3622818">Rhombus: A New Spin on Macros without All the Parentheses ...</a></li>

</ul>
</details>

**社区讨论**: 讨论中包含了来自核心贡献者（如 Matthew Flatt）的专业评论。用户重点介绍了 `...` 操作符等特定功能（这是一个宏，而非内置的展开操作），并引用了解释性视频和 Shrubbery 语法模块，这显示了深度的技术参与，而非广泛的辩论。

**标签**: `#programming languages`, `#Racket`, `#macros`, `#syntax`, `#language design`

---

<a id="item-16"></a>
## [关于医疗大模型 API 可用性的询问](https://www.reddit.com/r/MachineLearning/comments/1ue87js/could_it_be_that_there_arent_really_any_medical/) ⭐️ 6.0/10

一位 Reddit 用户对诸如 MedGemma 和 BioMistral 等医疗导向的大语言模型似乎缺乏公开可用的现成 API 表示惊讶，并明确表示不愿自行托管。 用户特别指出在 Hugging Face 上找到了模型但未找到公共 API；回应应阐明当前的托管现状，包括 Google MedGemma 等提供笔记本和微调支持但可能需要托管部署的选项。

reddit · r/MachineLearning · /u/Entrepreneur7962 · 6月24日 08:59

**背景**: 医疗大语言模型是在医疗数据上训练的 AI，用于医疗文本理解和图像解读等任务。虽然像 MedGemma（来自 Google）和 BioMistral 这样的模型已在 Hugging Face 等平台上以开源权重形式提供，但提供一个可立即使用的简单公共 API 端点是另一回事，许多项目尚未提供此服务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developers.google.com/health-ai-developer-foundations/medgemma">MedGemma | Health AI Developer Foundations | Google for ...</a></li>
<li><a href="https://github.com/google-health/medgemma">GitHub - Google-Health/medgemma</a></li>
<li><a href="https://github.com/GURPREETKAURJETHRA/Medical-RAG-using-Bio-Mistral-7B">Build a Medical RAG App using BioMistral, Qdrant, and Llama.cpp</a></li>

</ul>
</details>

**标签**: `#LLM`, `#medical-ai`, `#APIs`, `#research-tools`, `#machine-learning`

---