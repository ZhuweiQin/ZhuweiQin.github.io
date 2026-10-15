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

I am an **Associate Professor** of Computer Engineering in the College of Science & Engineering at **San Francisco State University (SFSU)**, where I direct the [Mobile and Intelligent Computing (MIC) Laboratory](http://sfsu-miclab.org/). I am also an Adjunct Faculty member in Electrical and Computer Engineering at George Mason University, teaching graduate courses on mobile systems and distributed & federated learning. I received my Ph.D. in Electrical and Computer Engineering from George Mason University in 2020.

My research makes AI **efficient, adaptive, and deployable** on resource-constrained devices, and applies it to human-machine interfaces and engineering education. I have published 38 papers in venues such as IEEE TCAD, KDD, IJCAI, ICCAD, DATE and BMVC (900+ citations), and have been funded by the NSF, the Department of Defense, Sony, and SFSU (13 projects, about $2.0M).

**Research interests:**
- **Efficient AI Computing** — edge & mobile model acceleration, LLM compression and domain adaptation, federated & decentralized learning
- **Intelligent Sensing & Neural-Machine Interfaces** — high-density EMG gesture recognition, on-device learning for rehabilitation, wearable biomedical sensing
- **AI for Education** — human-centered and trustworthy AI, intelligent tutoring, support for neurodiverse students

</div>

<div class="bio-content" id="bio-zh" markdown="1" style="display:none">

*美国旧金山州立大学 理工学院 计算机工程系 副教授*

秦柱伟，美国旧金山州立大学理工学院计算机工程系副教授，移动与智能计算实验室（MIC Lab）负责人，兼任美国乔治梅森大学电子与计算机工程系兼职教员，讲授移动系统、分布式与联邦学习等研究生课程。2020 年获乔治梅森大学电子与计算机工程博士学位。

主要研究高效、自适应、可部署于资源受限设备的人工智能技术，及其在人机接口和工程教育中的应用。已发表学术论文 38 篇，成果发表于 IEEE TCAD、KDD、IJCAI、ICCAD、DATE、BMVC 等期刊和会议，Google Scholar 引用 900 余次；主持或作为 Co-PI 承担美国国家科学基金会（NSF）、美国国防部、索尼公司等资助项目 13 项，总经费约 200 万美元，其中牵头负责两项在研 NSF 人工智能项目的 AI 部分。

**研究方向：**
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
