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


selected_papers: false
announcements:
  enabled: false
  scrollable: true
  limit: 5
---
<script>
  // Change the main heading to Chinese
  const nameHeading = document.querySelector(
    ".post-header .post-title"
  );

  if (nameHeading) {
    nameHeading.textContent = "罗桂波";
  }
</script>
北京大学信息工程学院助理教授/研究员、博士生导师，海外高层次人才，广东省高层次人才，“鹏城孔雀计划”特聘岗位专家。曾在哈佛大学医学院/麻省总医院从事博士后研究工作近4年。主要从事医学大模型、生理信号智能分析与多机构医学数据隐私协同计算研究。重点围绕大模型训练与推理优化、脑电及多模态生理行为建模、医学影像精准分割与诊断，以及基础模型与轻量模型协同优化等关键问题开展研究。相关方法已应用于神经发育疾病评估、智能健康监测，以及面向特殊人群的智能陪伴与干预辅助等场景。获得北京大学第二十四届青年教师教学基本功比赛优秀奖，获ACL SAC Highlights奖, MICCAI Best Paper Shortlist。发表了包括IEEE TPAMI、IEEE JBHI、Radiology: AI、IEEE TCSVT、IEEE TCDS、Journal of Digital Imaging、CVPR、ECCV、AAAI、ACL、USENIX 、ICSE 、IJCAI、MICCAI等国际顶级期刊和会议论文100多篇。

<div style="clear: both;"></div>

<!-- 中文学术动态 -->
<h2>
  <a href="{{ '/news/' | relative_url }}"
     style="color: inherit;">
    学术动态
  </a>
</h2>

{% assign all_news = site.data.news | sort: "date" | reverse %}

<div class="news">
  <div class="table-responsive">
    <table class="table table-sm table-borderless">
      {% for item in all_news limit: 5 %}
        <tr>
          <th scope="row"
              style="width: 150px; white-space: nowrap;">
            {{ item.date | date: "%Y年%m月%d日" }}
          </th>
          <td>
            {% assign news_text = item.text_zh | default: item.text %}
            {{ news_text | markdownify | remove: '<p>' | remove: '</p>' }}
          </td>
        </tr>
      {% endfor %}
    </table>
  </div>
</div>

<!-- 中文代表性论文 -->
<h2>
  <a href="{{ '/publications/' | relative_url }}"
     style="color: inherit;">
    代表性论文
  </a>
</h2>

{% include selected_papers.liquid %}

