---
layout: single
title: "Research"
permalink: /research/
author_profile: true
---

<div class="bio-switch">
  <button class="bio-btn active" data-lang="en">EN</button>
  <button class="bio-btn" data-lang="zh">中文</button>
</div>

<div class="bio-content" id="research-en" markdown="1">

## Research Directions

My research makes AI **efficient, adaptive, deployable and trustworthy** on resource-constrained devices. It spans three mutually reinforcing directions:

1. **Efficient AI Computing** — edge and mobile model acceleration, compression and domain adaptation of large language models, and federated and decentralized collaborative learning;
2. **Intelligent Sensing & Neural-Machine Interfaces** — real-time gesture recognition from high-density EMG, on-device learning and adaptation, and neural-controlled rehabilitation and prosthetic systems;
3. **AI for Education** — human-centered, trustworthy AI systems, intelligent tutoring platforms, and support for neurodiverse students.

## Key Achievements

38 publications, including 4 CCF-A, 4 CCF-B and 8 CCF-C papers, in venues such as IEEE TCAD, KDD, IJCAI, ICCAD, DATE and BMVC (900+ citations on Google Scholar, h-index 12). PI or Co-PI on 13 funded projects from the NSF, the Department of Defense, Sony and others, totaling about $2.0M, including leading the AI components of two active NSF AI projects. Recipient of the DAC Richard Newton Young Fellow Award and the ACM/IEEE SEC Best Poster Award; NSF panelist and program committee member for DAC and ASP-DAC.

## Research Contributions

1. **Interpretability-driven model compression and dynamic reconfiguration.** Starting from the functional semantics of convolutional filters, I established a "visual interpretation → function identification → structural compression" pipeline, leading to class-adaptive network reconfiguration (CAPTOR/CAPTORX) and functionality-oriented filter pruning that tailor models to the task and device budget. I recently extended this line of work to large language models with EfficientXpert, a propagation-aware pruning method for low-cost domain adaptation.
2. **Collaborative and federated learning on heterogeneous edge devices.** To address heterogeneity in compute, data and tasks across edge devices, we proposed feature-aligned federated aggregation (Fed2), which mitigates the feature misalignment caused by conventional parameter averaging, and studied task-adaptive incremental learning and decentralized collaborative training so that devices can learn together while keeping data local.
3. **On-device adaptive neural-machine interfaces.** I built an end-to-end pipeline from robust sensing to lightweight inference to on-device adaptation: GAN-based augmentation for robust HD-EMG recognition, efficient recognition networks for embedded hardware, and on-device online learning (mMyoHMI, EdgeEMG, NeuroEdge). Deployed with Sony on low-power microcontrollers, these techniques support rehabilitation exoskeletons and neural-controlled bionic arms.
4. **Human-centered AI for education.** I developed the AI Collaborative teaching platforms (AICO/SCAPE), piloted in engineering courses, to advance trustworthy and explainable AI in education.

</div>

<div class="bio-content" id="research-zh" markdown="1" style="display:none">

## 研究方向

长期从事智能计算研究，致力于解决深度学习模型在资源受限设备上“部署难、适应难、可信难”的问题，形成三个相互支撑的研究方向：

1. **高效人工智能计算**：边缘与移动端深度模型加速、大语言模型压缩与领域适配、联邦学习与去中心化协同学习；
2. **智能感知与人机接口**：基于高密度肌电的实时手势识别、端侧学习与自适应、神经控制康复与假肢系统；
3. **人工智能赋能工程教育**：以人为中心的可信AI系统、智能辅导平台、神经多样性学生支持。

## 主要成果

已发表学术论文38篇，其中CCF-A类4篇、CCF-B类4篇、CCF-C类8篇，代表性成果发表于IEEE TCAD、KDD、IJCAI、ICCAD、DATE、BMVC等，Google Scholar引用900余次，h指数12。主持或作为Co-PI承担美国国家科学基金会（NSF）、美国国防部、索尼公司等资助的科研项目13项，总经费约200万美元，其中牵头负责两项在研NSF人工智能项目的AI部分。曾获DAC Richard Newton青年学者奖、ACM/IEEE SEC最佳海报奖；担任NSF项目评审专家及DAC、ASP-DAC程序委员会委员。

## 学术创新点

1. **可解释性驱动的模型压缩与动态重构**：从卷积滤波器的功能语义出发，建立“可视化解释—功能识别—结构压缩”的技术路线，提出按任务类别自适应重构网络的方法（CAPTOR/CAPTORX）和面向功能的滤波器剪枝，使模型可根据任务与设备资源按需裁剪；近期将该思路拓展至大语言模型，提出传播感知剪枝方法EfficientXpert，实现低成本领域适配。
2. **面向异构边缘设备的协同与联邦学习**：针对边缘设备在算力、数据与任务上的异构性，提出特征对齐的联邦聚合方法（Fed2），缓解传统参数平均导致的特征错位；并研究任务自适应增量学习与去中心化协同训练，支持多设备在数据不出本地的前提下协同演进。
3. **端侧自适应的神经-机器接口**：打通“鲁棒感知—轻量推理—端侧自适应”全流程，利用生成对抗网络增强高密度肌电识别的鲁棒性，设计面向嵌入式设备的高效识别网络，并实现端侧在线学习与自适应（mMyoHMI、EdgeEMG、NeuroEdge），并与索尼公司合作部署于低功耗微控制器，应用于康复外骨骼与神经控制仿生手臂。
4. **以人为中心的教育AI系统**：研发AI协同教学平台（AICO/SCAPE）并在工程课程中试点应用，推动AI在教育场景中可信、可解释地落地。

</div>

<script>
(function () {
  var btns = document.querySelectorAll('.bio-btn');
  var TITLES = { en: 'Research', zh: '研究概述' };
  function show(lang) {
    document.getElementById('research-en').style.display = lang === 'en' ? '' : 'none';
    document.getElementById('research-zh').style.display = lang === 'zh' ? '' : 'none';
    var t = document.querySelector('.page__title'); if (t) t.textContent = TITLES[lang];
    btns.forEach(function (b) { b.classList.toggle('active', b.dataset.lang === lang); });
    try { localStorage.setItem('bio-lang', lang); } catch (e) {}
  }
  btns.forEach(function (b) { b.addEventListener('click', function () { show(b.dataset.lang); }); });
  var init = location.hash === '#zh' ? 'zh' : null;
  if (!init) { try { init = localStorage.getItem('bio-lang'); } catch (e) {} }
  show(init === 'zh' ? 'zh' : 'en');
})();
</script>
