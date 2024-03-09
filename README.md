<div class="Box-sc-g0xbh4-0 bJMeLZ js-snippet-clipboard-copy-unpositioned" data-hpc="true"><article class="markdown-body entry-content container-lg" itemprop="text"><div class="markdown-heading" dir="auto"><h1 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Zooids：Swarm 用户界面的构建块 \ 扩展材料</font></font></h1><a id="user-content-zooids-building-blocks-for-swarm-user-interfaces---extended-material" class="anchor" aria-label="永久链接：Zooids：Swarm 用户界面的构建块 \ 扩展材料" href="#zooids-building-blocks-for-swarm-user-interfaces---extended-material"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><a target="_blank" rel="noopener noreferrer" href="https://github.com/ShapeLab/SwarmUI/blob/master/Images/Teaser3.png"><img src="https://github.com/ShapeLab/SwarmUI/raw/master/Images/Teaser3.png" alt="预告片" style="max-width: 100%;"></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">
本文介绍了群体用户界面，这是一种新型人机界面，由许多处理显示和交互的自主机器人组成。</font><font style="vertical-align: inherit;">我们描述了 Zooids 的设计，这是一个用于开发桌面群体接口的开源硬件平台。</font><font style="vertical-align: inherit;">该平台由一系列定制设计的轮式微型机器人（直径为 2.6 厘米）、无线电基站、用于光学跟踪的高速 DLP 结构光投影仪以及用于应用程序开发和控制的软件框架组成。</font><font style="vertical-align: inherit;">我们通过一组使用 Zooids 开发的应用场景来说明桌面群体用户界面的潜力，并讨论群体用户界面特有的一般设计注意事项。</font></font></p>
<p dir="auto"><a href="http://www.youtube.com/watch?v=ZVdAfDMP3m0" title="Zooids：Swarm 用户界面的构建块" rel="nofollow"><img src="https://camo.githubusercontent.com/3bee0489138edba874e6cf439c3a4bcedaaae1c3a01f7bc495caf2de868409f0/687474703a2f2f696d672e796f75747562652e636f6d2f76692f5a56644166444d50336d302f302e6a7067" alt="图片替代文字" data-canonical-src="http://img.youtube.com/vi/ZVdAfDMP3m0/0.jpg" style="max-width: 100%;"></a></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">硬件</font></font></h2><a id="user-content-hardware" class="anchor" aria-label="永久链接：硬件" href="#hardware"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p align="center" dir="auto">
<a target="_blank" rel="noopener noreferrer" href="https://github.com/ShapeLab/SwarmUI/blob/master/Images/exploded.PNG"><img src="https://github.com/ShapeLab/SwarmUI/raw/master/Images/exploded.PNG" alt="爆炸了" width="400" style="max-width: 100%;"></a>
</p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Zooids 是小型定制机器人，如上图所示；</font><font style="vertical-align: inherit;">它们的尺寸为直径 26 毫米，高 21 毫米，重量约 12 克。</font><font style="vertical-align: inherit;">每个机器人均由 100 mAh 锂聚合物电池供电，并使用电机驱动轮。</font><font style="vertical-align: inherit;">它包含用于电容式触摸感应的柔性电极。</font><font style="vertical-align: inherit;">它通过NRF24L01+芯片与主计算机通信。</font></font></p>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">追踪</font></font></h3><a id="user-content-tracking" class="anchor" aria-label="永久链接：跟踪" href="#tracking"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">我们的系统使用基于投影仪的跟踪系统来进行机器人位置跟踪，如下所示。</font><font style="vertical-align: inherit;">使用 Texas Instruments Inc. 的高帧速率 (3000Hz) 投影仪 (DLP LightCrafter)，将一系列格雷编码图案投影到平坦表面上。</font><font style="vertical-align: inherit;">然后，机器人上的光电二极管独立解码到投影区域内的位置。</font><font style="vertical-align: inherit;">设置此基于投影仪的跟踪系统的说明包含在存储库中。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">软件</font></font></h2><a id="user-content-software" class="anchor" aria-label="永久链接：软件" href="#software"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p align="center" dir="auto">
<a target="_blank" rel="noopener noreferrer" href="https://github.com/ShapeLab/SwarmUI/blob/master/Images/architecture.PNG"><img src="https://github.com/ShapeLab/SwarmUI/raw/master/Images/architecture.PNG" alt="建筑学" width="700" style="max-width: 100%;"></a>
</p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">通信结构由四个主要层组成，从最高到最低级别：应用程序、模拟、服务器和硬件。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在应用程序级别，计算机器人的所需位置。</font><font style="vertical-align: inherit;">这些所需的位置通过网络套接字传输到模拟层。</font><font style="vertical-align: inherit;">应用程序员可以在两种控制策略之间进行选择：比例积分微分 (PID) 位置控制或混合倒数速度障碍 (HRVO) 与 PID 相结合（这些选项将在下一段中解释）。</font><font style="vertical-align: inherit;">根据所选的控制策略，模拟层计算机器人的目标位置（PID 的最终位置或 HRVO 的中间点），并将其发送到服务器。</font><font style="vertical-align: inherit;">最后，服务器层向各个zooid发送命令，同时监视它们的状态和位置。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">每个机器人通过基于如下所示状态机的 PID 控制器独立控制其运动。</font><font style="vertical-align: inherit;">给定最终目标，机器人最初会朝正确的方向转动，一旦对齐，就会加速到用户定义的首选速度。</font><font style="vertical-align: inherit;">当它达到该速度时，它会通过 PID 控制来保持该速度，以确保其朝向最终目标的方向。</font><font style="vertical-align: inherit;">当给出新的增量目标时，它仍将以相同的速度移动，但方向上的 PID 控制将引导机器人朝着新的中间目标前进。</font><font style="vertical-align: inherit;">当机器人到达距离最终目标 5 厘米以内时，它会减速到最小速度，一旦距离最终目标 1 厘米以内，它就会停止并按照应用程序员的命令调整自身方向。</font><font style="vertical-align: inherit;">为了实现增量目标位置之间的平滑过渡，机器人以 60 Hz 的频率获得下一个位置。</font></font></p>
<p align="center" dir="auto">
<a target="_blank" rel="noopener noreferrer" href="https://github.com/ShapeLab/SwarmUI/blob/master/Images/local_control.PNG"><img src="https://github.com/ShapeLab/SwarmUI/raw/master/Images/local_control.PNG" alt="控制" width="700" style="max-width: 100%;"></a>
</p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">致谢</font></font></h2><a id="user-content-acknowledgments" class="anchor" aria-label="永久链接：致谢" href="#acknowledgments"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">这是斯坦福大学（美国）Shape Lab 和 Inria（法国）Aviz 团队的合作成果。</font><font style="vertical-align: inherit;">该项目的部分资金由法兰西岛大区 DIM ISC-PIF 资助。</font><font style="vertical-align: inherit;">我们还要感谢 Alexa Siu、Shenli Yuan、Ernesto Ramirez 和 Pham Minh Hieu 投入大量时间和精力使这项工作成为可能。</font></font></p>
<p align="center" dir="auto">
<a target="_blank" rel="noopener noreferrer" href="https://github.com/ShapeLab/SwarmUI/blob/master/Images/logos.png"><img src="https://github.com/ShapeLab/SwarmUI/raw/master/Images/logos.png" alt="标志" width="700" style="max-width: 100%;"></a>
</p>
<p dir="auto"><a href="http://creativecommons.org/licenses/by-sa/4.0/" rel="nofollow"><img alt="知识共享许可" src="https://camo.githubusercontent.com/69e3e681f1cf6b155fc6148fc6d44d3fccc65dff25e654cba40733e10558bea9/68747470733a2f2f692e6372656174697665636f6d6d6f6e732e6f72672f6c2f62792d73612f342e302f38387833312e706e67" data-canonical-src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" style="max-width: 100%;"></a><br><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">本作品根据</font></font><a href="http://creativecommons.org/licenses/by-sa/4.0/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Creative Commons Attribution-ShareAlike 4.0 International License</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">获得许可。</font></font></p>
</article></div>
