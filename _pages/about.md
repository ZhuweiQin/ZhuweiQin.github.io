---
permalink: /
title: "Zhuwei Qin"
author_profile: true
redirect_from:
  - /about/
  - /about.html
  - /zh/
---

<div class="bio-switch">
  <button class="bio-btn active" data-lang="en">EN</button>
  <button class="bio-btn" data-lang="zh">中文</button>
</div>

<div class="bio-content" id="bio-en" markdown="1">

*Associate Professor, Computer Engineering, College of Science & Engineering, San Francisco State University*

Zhuwei Qin received his Ph.D. in Electrical and Computer Engineering from George Mason University in August 2020 under the guidance of [Dr. Xiang Chen](https://if-lab-pku.github.io/). Right after his Ph.D., he joined the Computer Engineering faculty at **San Francisco State University (SFSU)**, where he has since earned tenure. His research makes AI **efficient, adaptive, deployable and trustworthy** on resource-constrained mobile devices, and applies it to human-machine interfaces and engineering education. He has been PI or Co-PI on 13 projects funded by the NSF, the Department of Defense, Sony and others, totaling about $2.0M, including leading the AI components of two ongoing NSF AI projects. He has published 38 papers in venues such as IEEE TCAD, KDD, IJCAI, ICCAD, DATE and BMVC, with 900+ Google Scholar citations.

**Currently, Prof. Qin's main research directions:**
- **Efficient AI Computing** — edge & mobile model acceleration, LLM compression and domain adaptation, federated & decentralized learning
- **Intelligent Sensing & Neural-Machine Interfaces** — high-density EMG gesture recognition, on-device learning for rehabilitation, wearable biomedical sensing
- **AI for Education** — human-centered and trustworthy AI, intelligent tutoring, support for neurodiverse students

</div>

<div class="bio-content" id="bio-zh" markdown="1" style="display:none">

*美国旧金山州立大学 理工学院 计算机工程系 副教授*

秦柱伟，师从[陈翔教授](https://if-lab-pku.github.io/)，2020 年 8 月获乔治梅森大学电子与计算机工程博士学位。博士毕业后，即在美国旧金山州立大学的计算机工程系任教并获得终身教职。他的研究工作主要致力于让人工智能在资源受限的移动设备上更加高效、自适应、可部署、可信，并将其应用于人机接口和工程教育。主持或作为 Co-PI 承担美国国家科学基金会（NSF）、美国国防部、索尼公司等资助项目 13 项，总经费约 200 万美元，其中牵头负责两项在研 NSF 人工智能项目的 AI 部分。已发表学术论文 38 篇，成果发表于 IEEE TCAD、KDD、IJCAI、ICCAD、DATE、BMVC 等期刊和会议，Google Scholar 引用 900 余次。

**目前，秦柱伟教授的主要研究方向：**
- **高效人工智能计算（Efficient AI Computing）**：边缘与移动端模型加速、大语言模型压缩与领域适配、联邦学习与去中心化学习
- **智能感知与人机接口（Intelligent Sensing & Neural-Machine Interfaces）**：高密度肌电实时手势识别、神经-机器接口与康复系统、可穿戴生物医学感知
- **人工智能赋能工程教育（AI for Education）**：以人为中心的可信 AI、智能辅导系统、神经多样性学生支持

</div>

Join Us
======
I am looking for **motivated students** interested in **efficient AI, on-device learning, and intelligent sensing / human-machine interfaces**. Experience with PyTorch, embedded systems, or signal processing is a plus. Please email me at **zwqin#sfsu.edu** (replace # with @) with your CV.

Selected Recent Publications
======
Full list [HERE](/publications/).

{% include selected-pubs.html %}

Awards and Honors
======
- ***Richard Newton Young Fellow Award*** — DAC, 2017. *54th ACM/IEEE Design Automation Conference*
- ***Best Poster Award*** — SEC, 2019. *4th ACM/IEEE Symposium on Edge Computing*
- ***First Prize*** — IEEE Services Hackathon, 2020
- ***Grand Prize*** (as faculty advisor) — Sony Spresense Developer Challenge, 2022
- ***First Place*** (as faculty advisor) — KumoRFM Hackathon Challenge, 2025
- ***SFSU Campus-wide Winner*** (as faculty advisor) — CSU Student Research Competition, 2025

<script>
(function () {
  var btns = document.querySelectorAll('.bio-btn');
  var NAMES = { en: 'Zhuwei Qin', zh: '秦柱伟' };
  function setName(lang) {
    document.querySelectorAll('.page__title, .author__name').forEach(function (el) { el.textContent = NAMES[lang]; });
  }
  function show(lang) {
    setName(lang);
    document.getElementById('bio-en').style.display = lang === 'en' ? '' : 'none';
    document.getElementById('bio-zh').style.display = lang === 'zh' ? '' : 'none';
    btns.forEach(function (b) { b.classList.toggle('active', b.dataset.lang === lang); });
    try { localStorage.setItem('bio-lang', lang); } catch (e) {}
  }
  btns.forEach(function (b) { b.addEventListener('click', function () { show(b.dataset.lang); }); });
  var init = location.hash === '#zh' ? 'zh' : null;
  if (!init) { try { init = localStorage.getItem('bio-lang'); } catch (e) {} }
  show(init === 'zh' ? 'zh' : 'en');
})();
</script>
