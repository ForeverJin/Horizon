---
layout: default
title: "Horizon Summary: 2026-06-24 (EN)"
date: 2026-06-24
lang: en
---

> From 37 items, 16 important content pieces were selected

---

1. [Pico W Becomes Driverless USB Wi-Fi Adapter](#item-1) ⭐️ 8.0/10
2. [Qwen-AgentWorld: Language World Models for General Agents](#item-2) ⭐️ 8.0/10
3. [Research: LLMs Confuse Roles, Fail at Prompt Injection Defense](#item-3) ⭐️ 8.0/10
4. [Porting Moebius 0.2B Inpainting Model to Browser with WebGPU](#item-4) ⭐️ 8.0/10
5. [DeepSWE: A New Benchmark for Evaluating LLMs on Real-World Software Engineering](#item-5) ⭐️ 8.0/10
6. [LLM-Driven Vulnerability Reporting Challenges Security Disclosure Norms](#item-6) ⭐️ 7.0/10
7. [MacBook Neo Cursor Lag Workaround: Record a Single Pixel Every 10 Seconds](#item-7) ⭐️ 7.0/10
8. [Apple Acquires Swift Package Index](#item-8) ⭐️ 7.0/10
9. [Datasette 1.0a35 Adds Table Creation & Alteration](#item-9) ⭐️ 7.0/10
10. [Practitioner Questions ML Teams' Security Testing Gap](#item-10) ⭐️ 7.0/10
11. [Papers with Code Revival Adds SOTA Badges and New Trending Score](#item-11) ⭐️ 7.0/10
12. [uv 0.11.24 Adds Python 3.15 Beta Support](#item-12) ⭐️ 6.0/10
13. [BunnyNet Makes DNS Service Free for Up to 500 Domains](#item-13) ⭐️ 6.0/10
14. [FUTO Introduces Open-Source Swipe Typing Model](#item-14) ⭐️ 6.0/10
15. [Rhombus Language 1.0 Released on Racket](#item-15) ⭐️ 6.0/10
16. [Query on Medical LLM API Availability](#item-16) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Pico W Becomes Driverless USB Wi-Fi Adapter](https://gitlab.com/baiyibai/pico-usb-wifi) ⭐️ 8.0/10

A new firmware project allows the Raspberry Pi Pico W microcontroller to emulate a USB CDC-NCM device, turning it into a plug-and-play Wi-Fi adapter for computers. 该项目提供了一种低成本、开源的解决方案，可以为仅有 USB 接口的设备（如旧式台式机或嵌入式系统）添加无线连接，且无需安装定制驱动程序。 The firmware works by having the Pico W enumerate as a standard USB Ethernet adapter using the CDC-NCM protocol, which is natively supported by most modern operating systems.

hackernews · byb · Jun 24, 03:17 · [Discussion](https://news.ycombinator.com/item?id=48654676)

**Background**: The Raspberry Pi Pico W is a low-cost, programmable microcontroller with onboard Wi-Fi. CDC-NCM is a USB class specification that allows a device to present itself as a network adapter without needing a specific driver.

<details><summary>References</summary>
<ul>
<li><a href="https://www.raspberrypi.com/documentation/microcontrollers/raspberry-pi-pico.html">Pico microcontroller boards - Raspberry Pi Documentation</a></li>
<li><a href="https://docs.silabs.com/protocol-usb/1.6.0/protocol-usb-cdc/">USB Device CDC ACM Class - Developer Docs - Silicon Labs</a></li>

</ul>
</details>

**Discussion**: The community discussion praised the project's use of GitLab as an alternative to GitHub, shared related projects like using a Pico W as a travel router, and noted that similar USB-to-Ethernet emulation techniques have been used in other retro-computing projects.

**Tags**: `#hardware`, `#firmware`, `#raspberry-pi`, `#networking`, `#open-source`

---

<a id="item-2"></a>
## [Qwen-AgentWorld: Language World Models for General Agents](https://arxiv.org/abs/2606.24597) ⭐️ 8.0/10

Researchers have proposed Qwen-AgentWorld, a language-based world model designed to help AI agents simulate and plan in open-ended environments, and released an open-weight 35B-parameter model. The model is notable as the first language world model to cover seven unified agent interaction domains within a single architecture. This development is significant because it provides a native world model that can improve AI agents' ability to track workflow state, plan actions, and verify execution paths against constraints. It could reduce errors and the need for constant manual reminders in complex, multi-step agent workflows, impacting fields like automation and robotics. The released model, Qwen-AgentWorld-35B-A3B, is a Mixture-of-Experts (MoE) model with 35B total parameters but only 3B active parameters during inference, making it more efficient. Environment modeling is trained as the native objective from the continuous pre-training stage, rather than being added as a post-hoc component.

hackernews · ilreb · Jun 24, 02:21 · [Discussion](https://news.ycombinator.com/item?id=48654351)

**Background**: A world model for AI agents is a system that predicts how an environment will change based on the agent's current observations and planned actions. It acts as an internal simulator, allowing an agent to mentally 'rehearse' or plan sequences of steps before executing them in the real world, which is a core mechanism for reasoning and planning. Language world models aim to perform this simulation using natural language representations, potentially making them more flexible and interpretable.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2606.24597">Qwen-AgentWorld: Language World Models for General Agents - arXiv</a></li>
<li><a href="https://github.com/QwenLM/Qwen-AgentWorld/tree/main">GitHub - QwenLM/Qwen-AgentWorld: Qwen-AgentWorld: Language ...</a></li>
<li><a href="https://www.reddit.com/r/LocalLLaMA/comments/1ue5149/qwenagentworld35ba3b_a_3bactive_moe_trained_to/">Qwen-AgentWorld-35B-A3B: a 3B-active MoE trained to simulate ...</a></li>

</ul>
</details>

**Discussion**: The community discussion highlights several practical benefits, including improved workflow state tracking for smaller models and the potential to use the world model for verifying agent execution paths as a more reliable alternative to LLM-as-a-judge approaches. Some users also shared personal experiments with open-ended world simulation for agents, noting both the promise and challenges in simulating complex systems.

**Tags**: `#world models`, `#AI agents`, `#language models`, `#planning`, `#simulation`

---

<a id="item-3"></a>
## [Research: LLMs Confuse Roles, Fail at Prompt Injection Defense](https://simonwillison.net/2026/Jun/22/prompt-injection-as-role-confusion/#atom-everything) ⭐️ 8.0/10

Research by Charles Ye, Jasmine Cui, and Dylan Hadfield-Menell confirms that current LLMs cannot reliably distinguish between privileged system text and untrusted user input. They found that models rely heavily on the style of text rather than its content, leading to a vulnerability they term 'role confusion', which enables concerning jailbreak attacks. This finding confirms a fundamental architectural weakness in how LLMs handle trusted versus untrusted instructions, which is a core issue in AI security. It means that current prompt injection defenses may be perpetually insufficient, allowing attackers to manipulate models into generating harmful content at scale. The research demonstrated that 'destyling' a text—rewriting it in a format that doesn't match the expected role tag style—caused the attack success rate to plummet from 61% to 10%. The authors conclude that until LLMs achieve genuine role perception, injection defense will remain a 'perpetual whack-a-mole game'.

rss · Simon Willison · Jun 22, 23:59

**Background**: Prompt injection is a top security vulnerability where attackers craft inputs to trick an AI model into ignoring its safety instructions and following malicious commands. LLMs use special role tags like `<system>` and `<user>` to separate trusted instructions from untrusted user data, but this research shows that models often prioritize text style over this structural separation, making them susceptible to manipulation.

<details><summary>References</summary>
<ul>
<li><a href="https://genai.owasp.org/llmrisk/llm01-prompt-injection/">LLM01:2025 Prompt Injection - OWASP Gen AI Security Project</a></li>
<li><a href="https://engisphere.com/the-illusion-of-role-separation-in-llms-why-ai-struggles-to-distinguish-between-system-and-user-roles-and-how-to-fix-it/">The Illusion of Role Separation in LLMs | Why AI Struggles to ...</a></li>
<li><a href="https://www.boozallen.com/insights/ai-research/how-to-protect-llms-from-jailbreaking-attacks.html">How to Protect LLMs from Jailbreaking Attacks - Booz Allen</a></li>

</ul>
</details>

**Discussion**: The original post references a Hacker News discussion, though the comments were not provided for analysis. The author, Simon Willison, himself praises the value of the paper's accessible blog-style writeup, noting that academic writing's impact could be much higher if such summaries were standard practice.

**Tags**: `#AI Safety`, `#Prompt Injection`, `#LLM Security`, `#AI Research`, `#Cybersecurity`

---

<a id="item-4"></a>
## [Porting Moebius 0.2B Inpainting Model to Browser with WebGPU](https://simonwillison.net/2026/Jun/22/porting-moebius/#atom-everything) ⭐️ 8.0/10

Simon Willison successfully ported the lightweight Moebius 0.2B image inpainting model to run directly in a web browser using WebGPU, creating a functional demo. The model was originally dependent on PyTorch and NVIDIA CUDA, but the new implementation allows it to operate client-side. This demonstration shows that even small, efficient AI models can be made accessible to a wider audience by running them entirely in the browser, eliminating the need for server-side GPU hardware. It showcases the practical potential of WebGPU for deploying machine learning models on the client-side, potentially reducing latency and costs for interactive AI applications. The porting process involved using ONNX Runtime Web on the WebGPU backend, a lower-level alternative to Transformers.js. The original model's weights were in fp32 format, and the ported version runs on hardware with WebGPU support, which is now available in major browsers.

rss · Simon Willison · Jun 22, 23:43

**Background**: Image inpainting is a technique where users mark specific regions of an image for removal, and an AI model generates new content to seamlessly fill those areas. The Moebius model is notable for its small size (0.2 billion parameters) while claiming performance on par with much larger 10-billion-parameter models. WebGPU is a modern web graphics and computing API that allows web applications to access GPU acceleration, making it feasible to run computationally intensive tasks like AI inference directly in the browser.

<details><summary>References</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Jun/22/porting-moebius/">Porting the Moebius 0.2B image inpainting model to run in the browser with Claude Code</a></li>
<li><a href="https://hustvl.github.io/Moebius/">Moebius Project Page</a></li>
<li><a href="https://news.ycombinator.com/item?id=48630171">Moebius: 0.2B image inpainting model with 10B-level performance | Hacker News</a></li>

</ul>
</details>

**Discussion**: The Hacker News discussion highlighted that the original model weights were in fp32 format, and commenters inquired whether lower-precision formats like fp16 had been tried to potentially improve performance or reduce memory usage. The project also sparked interest in the broader trend of running AI models client-side using technologies like WebGPU and Transformers.js.

**Tags**: `#AI/ML`, `#WebGPU`, `#Image Inpainting`, `#Browser Deployment`, `#Model Porting`

---

<a id="item-5"></a>
## [DeepSWE: A New Benchmark for Evaluating LLMs on Real-World Software Engineering](https://www.reddit.com/r/MachineLearning/comments/1ue0hlp/deepswe_new_benchmark_looking_at_how_well_todays/) ⭐️ 8.0/10

A new open-source benchmark called DeepSWE has been released to rigorously evaluate frontier LLMs on real-world software engineering tasks. It advances existing benchmarks by being contamination-free, highly diverse across 91 repositories and 5 languages, and focused on testing software behavior rather than code implementation details. This benchmark addresses critical limitations in current code generation evaluation, such as data contamination and lack of real-world complexity, providing a more reliable measure of how well frontier AI models can perform actual software engineering work. Its design could set a new standard for assessing coding agents and drive improvements in their practical capabilities. DeepSWE's prompts are about half the length of those in SWE-bench Pro, yet the solutions require 5.5 times more code and approximately twice as many output tokens. The benchmark's verifiers are hand-written to test functional behavior rather than matching specific code implementations, and all tasks were created from scratch to prevent contamination.

reddit · r/MachineLearning · /u/we_are_mammals · Jun 24, 02:03

**Background**: Evaluating large language models (LLMs) on code generation is crucial but challenging, with issues like test set contamination and benchmarks not reflecting real-world software complexity. Previous benchmarks like SWE-bench and SWE-bench Pro have been influential, but concerns about data leakage and the gap between benchmark performance and practical engineering persist. The field is actively seeking more robust, contamination-resistant evaluation methods.

<details><summary>References</summary>
<ul>
<li><a href="https://deepswe.datacurve.ai/">DeepSWE</a></li>
<li><a href="https://www.reddit.com/r/singularity/comments/1tt7t5t/the_new_benchmarks_like_deepswe_now_show_a_very/">The new benchmarks like DeepSWE now show a very big gap in ... - Reddit</a></li>
<li><a href="https://venturebeat.com/technology/deepswe-blows-up-the-ai-coding-leaderboard-crowns-gpt-5-5-and-finds-claude-opus-exploiting-a-benchmark-loophole">DeepSWE blows up the AI coding leaderboard, crowns GPT-5.5, and ...</a></li>

</ul>
</details>

**Discussion**: A related Reddit discussion notes that new benchmarks like DeepSWE reveal a significant performance gap between different frontier models. There is also commentary on the benchmark's execution, with one user suggesting that the DeepSWE results were run in a somewhat incompetent manner, indicating potential scrutiny over methodology.

**Tags**: `#benchmarking`, `#code-generation`, `#LLM-evaluation`, `#software-engineering`, `#AI-research`

---

<a id="item-6"></a>
## [LLM-Driven Vulnerability Reporting Challenges Security Disclosure Norms](https://words.filippo.io/vuln-reports/) ⭐️ 7.0/10

A blog post argues that the privileged status of vulnerability reports is eroding due to increased automation and spam, particularly from LLMs. The discussion highlights that receiving end companies are now flooded with automated and often low-quality reports, devaluing the process. This shift challenges the traditional software security ecosystem, forcing companies and researchers to rethink how they handle disclosures and potentially impacting the incentives for responsible bug hunting. It signals a broader transformation in software engineering and security practices driven by generative AI. The discussion is fueled by real-world experiences where companies receive unsolicited vulnerability reports, many of which are LLM-generated spam targeting superficial issues. The debate centers on whether this flood of reports diminishes their perceived value and complicates the work of legitimate security researchers.

hackernews · goranmoomin · Jun 23, 23:42 · [Discussion](https://news.ycombinator.com/item?id=48653216)

**Background**: Vulnerability disclosure is a critical process in cybersecurity where researchers report software flaws to vendors to ensure responsible fix and public notification. Traditionally, these reports were considered special and received careful attention, as they often came from human experts and required significant effort to discover. The rise of Large Language Models (LLMs) has automated bug-finding, leading to a surge in reports, some of which are spam or low-quality.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.qualys.com/product-tech/2025/02/07/the-impact-of-llms-on-cybersecurity-new-threats-and-solutions">LLMs in Cybersecurity: Understanding Threats and Solutions | Qualys</a></li>
<li><a href="https://www.cisa.gov/resources-tools/programs/coordinated-vulnerability-disclosure-program">Coordinated Vulnerability Disclosure Program | CISA</a></li>
<li><a href="https://www.sciencedirect.com/science/article/pii/S2667345225000082">Generative AI in cybersecurity: A comprehensive review of LLM applications and vulnerabilities - ScienceDirect</a></li>

</ul>
</details>

**Discussion**: Commenters express frustration with the influx of spam and low-quality reports, with some noting that the situation may be temporary as LLMs eventually improve software quality. Others argue that the real engineering challenge is to fundamentally overhaul software practices to eliminate entire classes of vulnerabilities, rather than just relying on automated discovery.

**Tags**: `#cybersecurity`, `#AI_impact`, `#software_engineering`, `#vulnerability_disclosure`, `#LLM`

---

<a id="item-7"></a>
## [MacBook Neo Cursor Lag Workaround: Record a Single Pixel Every 10 Seconds](https://gist.github.com/retroplasma/ec21767d0a8380c7ea9c2fbee1c7d6bf) ⭐️ 7.0/10

A user discovered a creative but hacky workaround for cursor lag on the MacBook Neo by periodically recording a single pixel of the screen every 10 seconds. This action appears to force the operating system to switch from hardware-accelerated cursor rendering to a software-based method, eliminating the lag. This workaround highlights a specific hardware/software interaction bug in a new Apple device and demonstrates how an unconventional method can bypass a GPU driver issue. It also brings attention to the problem, potentially encouraging Apple to implement a proper fix in a future software update. The fix is achieved by a script that periodically reads one pixel to /dev/null, which likely triggers the macOS WindowServer to composite the cursor as a software layer instead of using a faster hardware overlay. This is considered a 'terrible fix' by some as it's a resource-intensive workaround for a fundamental driver bug.

hackernews · retroplasma · Jun 24, 02:38 · [Discussion](https://news.ycombinator.com/item?id=48654465)

**Background**: Computer systems typically use hardware cursors for smooth, low-latency mouse pointer display, where the GPU renders the cursor as a separate overlay independent of the main screen rendering. When this fails due to a software or driver issue, the system may fall back to a software cursor, which can introduce lag if not handled correctly. The MacBook Neo appears to have an issue where the transition to or handling of this software cursor mode is flawed.

<details><summary>References</summary>
<ul>
<li><a href="https://gist.github.com/retroplasma/ec21767d0a8380c7ea9c2fbee1c7d6bf">Unlag Neo: Macbook Neo Cursor lag "fix" · GitHub</a></li>
<li><a href="https://news.ycombinator.com/item?id=48654465">"Fix" MacBook Neo Cursor Lag: Record 1 Pixel of the Screen Every 10 Seconds | Hacker News</a></li>
<li><a href="https://stackoverflow.com/questions/6957039/what-is-hardware-cursor-and-how-does-it-work">opengl - What is hardware cursor and how does it work ...</a></li>

</ul>
</details>

**Discussion**: The Hacker News discussion reveals that the community understands the technical mechanism: the lag likely occurs during a stalled transition from hardware to software cursor rendering. While some find the fix amusing and clever enough to force Apple's hand, others criticize it as a 'terrible' and inelegant workaround that forces unnecessary compositing.

**Tags**: `#macOS`, `#hardware-software interaction`, `#GPU driver`, `#workaround`, `#Hacker News`

---

<a id="item-8"></a>
## [Apple Acquires Swift Package Index](https://swiftpackageindex.com/blog/swift-package-index-joins-apple) ⭐️ 7.0/10

The popular community-driven Swift Package Index, which catalogs metadata for over 11,000 Swift packages, has officially been acquired by Apple. The acquisition was announced on the Swift Package Index blog, stating that little will change for developers in the near term. This move signifies Apple's commitment to strengthening the Swift ecosystem by integrating a key community resource into its official developer toolchain. It could lead to tighter integration with tools like Xcode and influence how Swift packages are discovered, managed, and distributed in the future. The Swift Package Index pledges to remain open source and maintain its core functionality of indexing and providing metadata for packages primarily hosted on GitHub. However, Apple's announcement explicitly mentions exploring directions like developer identity, which has raised some concerns among community members about future changes to the platform.

hackernews · JDevlieghere · Jun 23, 18:00 · [Discussion](https://news.ycombinator.com/item?id=48648779)

**Background**: The Swift Package Index is a third-party search engine and metadata service for Swift packages, helping developers find and evaluate dependencies. It is distinct from the official Swift Package Manager (SPM), which is the build tool for Swift code, and from the concept of a formal Swift Package Registry, which is a separate specification for hosting and distributing packages that Apple is also developing.

<details><summary>References</summary>
<ul>
<li><a href="https://9to5mac.com/2026/06/23/swift-package-index-joins-apple-pledges-to-remain-open-source/">Swift Package Index joins Apple, pledges to remain open ...</a></li>
<li><a href="https://swiftpackageindex.com/">Swift Package Index</a></li>
<li><a href="https://www.swift.org/packages/">Packages | Swift.org</a></li>

</ul>
</details>

**Discussion**: Community sentiment is mixed, with some users expressing optimism about the founders achieving success, while others voice skepticism about Apple's stewardship of open-source projects and developer services. A notable concern is that Apple might pivot the platform's focus, as hinted by the mention of developer identity, potentially moving away from its current community-driven model.

**Tags**: `#Swift`, `#Apple`, `#Package Management`, `#Open Source`, `#Developer Tools`

---

<a id="item-9"></a>
## [Datasette 1.0a35 Adds Table Creation & Alteration](https://simonwillison.net/2026/Jun/23/datasette/#atom-everything) ⭐️ 7.0/10

Datasette 1.0a35 introduces new UI interfaces and JSON APIs for creating and altering database tables directly within the tool. This pre-release adds major features including a "Create table" action and an "Alter table" action, backed by corresponding new API endpoints. This update significantly enhances Datasette's capability as a standalone database management tool, making it easier for developers to prototype and manipulate data schemas without external software. The addition of stable template context documentation also improves the platform's extensibility for custom UI development. The new "Create table" interface can define columns, primary keys, custom types, NOT NULL constraints, defaults, and foreign keys. The "Alter table" dialog allows adding, renaming, dropping, and reordering columns, changing column properties, and includes a "Drop table" button.

rss · Simon Willison · Jun 23, 21:34

**Background**: Datasette is a popular open-source tool for exploring and publishing data as interactive web pages and APIs, built on SQLite. Prior to this release, Datasette primarily focused on data exploration and read-only access, with write capabilities introduced gradually through earlier alpha releases. The new template context documentation establishes a stable API for customizing Datasette's core pages.

<details><summary>References</summary>
<ul>
<li><a href="https://simonwillison.net/2022/Dec/2/datasette-write-api/">Datasette’s new JSON write API: The first alpha of Datasette 1.0</a></li>
<li><a href="https://newreleases.io/project/github/simonw/datasette/release/1.0a35">simonw/datasette 1.0a35 on GitHub - NewReleases.io</a></li>
<li><a href="https://datasette.io/blog/2026/jump-menu/">The extensible "Jump to" menu in Datasette 1.0a30</a></li>

</ul>
</details>

**Tags**: `#open-source`, `#data-tools`, `#APIs`, `#database-management`, `#release-notes`

---

<a id="item-10"></a>
## [Practitioner Questions ML Teams' Security Testing Gap](https://www.reddit.com/r/MachineLearning/comments/1uddtws/are_model_security_risks_extraction_poisoning/) ⭐️ 7.0/10

A machine learning practitioner has raised the question of whether many teams shipping ML models are actually conducting adversarial testing for security risks like model extraction and poisoning before deployment. The discussion highlights a perceived gap between ML model security practices and established software security reviews. This matters because inadequate security testing for ML models can expose businesses to significant financial, reputational, and operational risks, including intellectual property theft and system manipulation. As AI becomes more integrated into critical applications, addressing this security gap is crucial for building trustworthy and robust AI systems. The news specifically mentions two primary security risks: model extraction, where an attacker attempts to steal or replicate a model by querying its API, and model poisoning, where an attacker manipulates training data or parameters to introduce malicious behavior. The discussion frames the lack of adversarial testing for these risks as a critical oversight in many production ML workflows.

reddit · r/MachineLearning · /u/Xorphian · Jun 23, 10:52

**Background**: Model extraction is an attack where a threat actor queries a target model's API extensively to train a surrogate model that mimics its function, effectively stealing intellectual property. Model poisoning involves contaminating training data or manipulating the training process to cause the model to learn incorrect or malicious patterns, potentially creating backdoors. Adversarial testing is a security practice that involves actively probing a system with simulated attacks to identify vulnerabilities before they are exploited by real adversaries.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ibm.com/docs/en/watsonx/saas?topic=atlas-extraction-attack">Extraction attack risk for AI - IBM Documentation</a></li>
<li><a href="https://owasp.org/www-project-machine-learning-security-top-10/docs/ML10_2023-Model_Poisoning">ML10:2023 Model Poisoning - OWASP Foundation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Adversarial_machine_learning">Adversarial machine learning - Wikipedia</a></li>

</ul>
</details>

**Discussion**: The post has generated discussion among practitioners, with the author noting that many ML teams they speak with skip adversarial testing. The community is engaging to share experiences on whether such security practices are actually implemented in real-world jobs, indicating a shared concern about the maturity of ML security operations.

**Tags**: `#ML security`, `#adversarial testing`, `#model deployment`, `#production risks`, `#MLOps`

---

<a id="item-11"></a>
## [Papers with Code Revival Adds SOTA Badges and New Trending Score](https://www.reddit.com/r/MachineLearning/comments/1ucm508/some_new_updates_to_papers_with_code_p/) ⭐️ 7.0/10

The Hugging Face team member announced a revival of Papers with Code, introducing new features such as SOTA badges that highlight top-performing papers and a new trending score that combines GitHub star velocity with Hugging Face artifact metrics. The platform also now supports external evaluations and is gradually adding more tasks, benchmarks, and evals from legacy data. These updates significantly enhance the discoverability and benchmarking of machine learning research, helping the community more effectively build upon each other's work. By integrating metrics from Hugging Face ecosystems, it creates a more comprehensive and dynamic ranking system for trending research papers. The new trending score is a combination of GitHub star velocity and the trending score of linked Hugging Face models, datasets, and Spaces, whereas the previous version only used GitHub stars. The SOTA badges are automatically displayed when a paper achieves a score within the top 3 of a given benchmark, and support for external evals allows viewing third-party evaluations not originally in the paper.

reddit · r/MachineLearning · /u/NielsRogge · Jun 22, 14:29

**Background**: Papers with Code is a widely-used machine learning research platform that aggregates papers, their associated code repositories, and benchmark results to help researchers track progress and find resources. It was previously owned by Meta but was retired in July 2025, with the domain redirecting to Hugging Face Trending Papers. SOTA (State-of-the-Art) badges are visual indicators that highlight models or papers achieving the best-known performance on specific benchmarks.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/paperswithcode">Papers with code · GitHub</a></li>
<li><a href="https://www.reddit.com/r/MachineLearning/comments/1ucm508/some_new_updates_to_papers_with_code_p/">Some new updates to Papers with Code [P] : r/MachineLearning - Reddit</a></li>
<li><a href="https://www.codesota.com/papers-with-code">Papers With Code Alternative: SOTA Leaderboards and Archived Data</a></li>

</ul>
</details>

**Discussion**: The provided content is a direct announcement from the developer and does not include community comments. Therefore, a summary of community discussion cannot be provided.

**Tags**: `#machine learning`, `#research tools`, `#papers with code`, `#open source`, `#ML infrastructure`

---

<a id="item-12"></a>
## [uv 0.11.24 Adds Python 3.15 Beta Support](https://github.com/astral-sh/uv/releases/tag/0.11.24) ⭐️ 6.0/10

The uv package manager version 0.11.24 has been released, adding support for CPython 3.15.0b3 and implementing a compact index for lazy version maps to improve performance. This release keeps uv at the forefront of Python tooling by supporting the latest beta Python version early, and the performance optimization benefits users with large dependency trees. The update also includes bug fixes for relocatable project environments (a preview feature) and tool installations, such as fixing conflicts in archive IDs and cleaning up partial installs.

github · github-actions[bot] · Jun 23, 21:16

**Background**: uv is an extremely fast Python package and project manager written in Rust, designed as a modern replacement for tools like pip, pyenv, and virtualenv. It focuses on speed and reliability for installing and managing Python dependencies.

<details><summary>References</summary>
<ul>
<li><a href="https://pydevtools.com/handbook/explanation/uv-complete-guide/">uv: A Complete Guide to Python's Fastest Package Manager</a></li>
<li><a href="https://docs.astral.sh/uv/getting-started/features/">Features | uv - docs.astral.sh</a></li>
<li><a href="https://github.com/astral-sh/uv">GitHub - astral-sh/uv: An extremely fast Python package and ...</a></li>

</ul>
</details>

**Tags**: `#python`, `#package-management`, `#release`, `#tools`, `#performance`

---

<a id="item-13"></a>
## [BunnyNet Makes DNS Service Free for Up to 500 Domains](https://bunny.net/blog/were-making-bunny-dns-free/) ⭐️ 6.0/10

BunnyNet is making its Bunny DNS service free, eliminating all query fees and offering free DNS hosting for up to 500 domains per account. This includes advanced features like smart records and health monitoring that were previously part of paid plans. This move provides developers and infrastructure teams with a cost-effective, potentially faster alternative to major DNS providers like Cloudflare, especially for projects on a tight budget. It also strengthens the landscape of EU-based tech services, which is increasingly important in the current geopolitical climate. The free tier includes scriptable smart records that can dynamically route traffic based on user location or latency, and built-in health monitoring for domain availability. However, there is a limit of 500 domains per account for the free hosting service.

hackernews · dabinat · Jun 24, 08:50 · [Discussion](https://news.ycombinator.com/item?id=48657030)

**Background**: BunnyNet is a Slovenia-based cloud services and CDN provider offering various tools for web performance and infrastructure. DNS (Domain Name System) is the fundamental internet service that translates human-readable domain names into IP addresses, and its performance directly impacts website loading speed and reliability. Providers like Cloudflare and AWS Route 53 are common paid alternatives in this space.

<details><summary>References</summary>
<ul>
<li><a href="https://bunny.net/dns/">Bunny DNS | The #1 Scriptable DNS Platform | bunny.net</a></li>
<li><a href="https://docs.bunny.net/dns">Bunny DNS - bunny.net Documentation</a></li>
<li><a href="https://hostbillapp.com/products-services/bunnynet/">Bunny.net DNS | HostBill | Billing & Automation Software for WebHosts</a></li>

</ul>
</details>

**Discussion**: The community discussion highlights positive sentiment, with users appreciating the value for money and viewing BunnyNet as a welcome EU-based alternative to US giants. However, there are also practical concerns raised about the domain import process being imperfect and the service's business model being organic rather than fueled by investor capital.

**Tags**: `#DNS`, `#Infrastructure`, `#Cloud Services`, `#EU Tech`, `#Developer Tools`

---

<a id="item-14"></a>
## [FUTO Introduces Open-Source Swipe Typing Model](https://swipe.futo.tech/) ⭐️ 6.0/10

FUTO has released FUTO Swipe, a new family of open, small, on-device models designed to improve the accuracy and speed of swipe typing on Android. The system includes a layout-agnostic encoder, a layout-specific decoder, a lightweight language model, and was trained on a newly released 1 million swipe dataset. This project contributes a free and private, fully offline alternative for swipe typing, potentially advancing keyboard input technology for privacy-conscious users. It also provides open models and data for developers to build upon, which could lead to further innovations in mobile text input. The FUTO Swipe system runs efficiently on-device with a small footprint, making it suitable for integration into apps like the FUTO Keyboard. The model family is designed to be layout-agnostic at its core, allowing for potential optimization for different keyboard arrangements.

hackernews · futohq · Jun 23, 17:50 · [Discussion](https://news.ycombinator.com/item?id=48648619)

**Background**: Swipe typing, also known as glide typing, is a text input method where users drag their finger across a virtual keyboard to type words, with the software predicting the intended word. Traditional swiping models often struggle with similar-looking word paths and don't always optimize the physical keyboard layout for the unique demands of this input style. AI-powered prediction is increasingly used to improve accuracy in modern keyboard apps.

<details><summary>References</summary>
<ul>
<li><a href="https://swipe.futo.tech/">FUTO Swipe</a></li>
<li><a href="https://www.productcool.com/product/futo-swipe">FUTO Swipe - Open models for on-device swipe typing | ProductCool</a></li>
<li><a href="https://sangaline.com/post/finding-an-optimal-keyboard-layout-for-swype/">Finding an Optimal Keyboard Layout for Swype | sangaline.com</a></li>

</ul>
</details>

**Discussion**: Community feedback is mixed but generally positive. Some users praise the model for making FUTO Keyboard a viable, privacy-focused alternative to Gboard, while others note it still has issues like random capitalization and poor contextual word suggestions. There is also historical interest in optimized keyboard layouts specifically designed for swiping.

**Tags**: `#input methods`, `#keyboard design`, `#AI prediction`, `#user experience`, `#mobile technology`

---

<a id="item-15"></a>
## [Rhombus Language 1.0 Released on Racket](https://blog.racket-lang.org/2026/06/rhombus-v1.0.html) ⭐️ 6.0/10

Rhombus Language 1.0, a new programming language with a unique macro system built on Racket, has been officially released. This stable version marks a significant milestone, delivering a novel macro-extensible language with conventional, infix-style syntax. This release offers a practical alternative to Lisp-style syntax while preserving powerful language extensibility, potentially attracting developers who find s-expressions daunting. It showcases an advanced synthesis of macro technology that could influence future language design and the Racket ecosystem. Rhombus achieves its macro system without traditional parentheses by using multiple binding spaces for context-specific sublanguages, as detailed in its academic paper. The language's performance characteristics are a documented consideration, as indicated by a dedicated performance page.

hackernews · Decabytes · Jun 22, 17:50 · [Discussion](https://news.ycombinator.com/item?id=48633473)

**Background**: Racket is a Lisp dialect and a platform specifically designed for creating new programming languages and implementing language-oriented programming. A core feature of Racket is its powerful macro system, which allows developers to extend the language's syntax and semantics. Rhombus builds upon this foundation, aiming to provide similar extensibility while using a more conventional, non-Lisp-style syntax.

<details><summary>References</summary>
<ul>
<li><a href="https://jeapostrophe.github.io/home/static/rhombus-2023.pdf">Rhombus: A New Spin on Macros without All the Parentheses</a></li>
<li><a href="https://dl.acm.org/doi/10.1145/3622818">Rhombus: A New Spin on Macros without All the Parentheses ...</a></li>

</ul>
</details>

**Discussion**: The discussion features knowledgeable commentary from core contributors like Matthew Flatt. Users highlight specific features such as the general `...` operator (a macro, not a built-in splat) and reference explanatory videos and the Shrubbery syntax module, showing deep technical engagement rather than broad debate.

**Tags**: `#programming languages`, `#Racket`, `#macros`, `#syntax`, `#language design`

---

<a id="item-16"></a>
## [Query on Medical LLM API Availability](https://www.reddit.com/r/MachineLearning/comments/1ue87js/could_it_be_that_there_arent_really_any_medical/) ⭐️ 6.0/10

A user on Reddit questioned the apparent lack of publicly available, ready-to-use APIs for medical-oriented large language models like MedGemma and BioMistral, expressing surprise and a desire to avoid self-hosting. 此询问凸显了研究人员和开发者在获取专用医疗AI模型进行消融研究等任务时面临的实际障碍，这可能会减缓医疗AI应用的创新步伐。 The user specifically noted finding models on Hugging Face but not public APIs; responses should clarify the current hosting landscape, including options like Google's MedGemma which offers notebooks and fine-tuning support but may require managed deployment.

reddit · r/MachineLearning · /u/Entrepreneur7962 · Jun 24, 08:59

**Background**: Medical LLMs are AI models trained on healthcare data for tasks like medical text comprehension and image interpretation. While models like MedGemma (from Google) and BioMistral are available as open weights on platforms like Hugging Face, providing a simple, public API endpoint for immediate use is a separate offering that many projects do not yet provide.

<details><summary>References</summary>
<ul>
<li><a href="https://developers.google.com/health-ai-developer-foundations/medgemma">MedGemma | Health AI Developer Foundations | Google for ...</a></li>
<li><a href="https://github.com/google-health/medgemma">GitHub - Google-Health/medgemma</a></li>
<li><a href="https://github.com/GURPREETKAURJETHRA/Medical-RAG-using-Bio-Mistral-7B">Build a Medical RAG App using BioMistral, Qdrant, and Llama.cpp</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#medical-ai`, `#APIs`, `#research-tools`, `#machine-learning`

---