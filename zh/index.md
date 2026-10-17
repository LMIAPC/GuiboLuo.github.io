---
layout: about
title: 中文
permalink: /zh/
lang: zh-CN
nav: false

subtitle: >-
  <span style="display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap; gap:8px; width:100%;">
    <a href="https://www.ece.pku.edu.cn/info/1062/2227.htm">北京大学</a>
    <a href="/">English Version / 英文版</a>
  </span>

profile:
  align: left
  image: lgb_pic.png
  image_circular: false

selected_papers: true
social: true
announcements:
  enabled: true
  scrollable: true
  limit: 5
---
<style>
  /* Hide the name in the top navbar on Chinese page */
  #navbar .navbar-brand.title {
    display: none !important;
  }
</style>

<script>
  // Change the main heading to Chinese
  const nameHeading = document.querySelector(
    ".post-header .post-title"
  );

  if (nameHeading) {
    nameHeading.textContent = "罗桂波";
  }
</script>

北京大学信息工程学院助理教授、博士生导师，曾在哈佛医学院及麻省总医院从事近四年的博士后研究。主要从事人工智能与医学智能交叉领域研究，包括医学基础模型、生理信号智能分析、隐私保护与跨机构协同学习等。研究工作涉及基础模型高效训练与推理、脑电及多模态生理行为建模、医学影像智能分割与辅助诊断，以及基础模型与轻量化模型的协同优化。研究成果发表于 IEEE TPAMI、IEEE JBHI、Radiology: AI、CVPR、ECCV、AAAI、ACL、USENIX Security、ICSE、IJCAI 和 MICCAI 等国际期刊及会议。

## 更多信息
[Publications]({{ '/publications/' | relative_url }}) |
[News]({{ '/news/' | relative_url }}) |
[Google Scholar](https://scholar.google.com/citations?user=kUIPmL4AAAAJ) |
[alphaXiv](https://www.alphaxiv.org/@guibo-luo)
