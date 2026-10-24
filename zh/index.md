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
<style>
  /* Reduce navbar height and move bottom line upward */
  #navbar {
    padding-top: 0 !important;
    padding-bottom: 0 !important;
  }

  /* Hide navbar name on Chinese page */
  #navbar .navbar-brand.title {
    display: none !important;
  }
</style>

<script>
  // Display Chinese name
  document.addEventListener("DOMContentLoaded", function () {
    const heading = document.querySelector(
      ".post-header .post-title"
    );
    if (heading) {
      heading.textContent = "罗桂波";
    }
  });
</script>
北京大学信息工程学院助理教授/研究员、博士生导师，海外高层次人才，广东省高层次人才，“鹏城孔雀计划”特聘岗位专家。曾在哈佛大学医学院/麻省总医院从事博士后研究工作近4年。主要从事医学大模型、生理信号智能分析与多机构医学数据隐私协同计算研究。重点围绕大模型训练与推理优化、脑电及多模态生理行为建模、医学影像精准分割与诊断，以及基础模型与轻量模型协同优化等关键问题开展研究。相关方法已应用于神经发育疾病评估、智能健康监测，以及面向特殊人群的智能陪伴与干预辅助等场景。获得北京大学第二十四届青年教师教学基本功比赛优秀奖，获ACL SAC Highlights奖, MICCAI Best Paper Shortlist。发表了包括IEEE TPAMI、IEEE JBHI、Radiology: AI、IEEE TCSVT、IEEE TCDS、Journal of Digital Imaging、CVPR、ECCV、AAAI、ACL、USENIX 、ICSE 、IJCAI、MICCAI等国际顶级期刊和会议论文100多篇。

团队现有成员20余人，包括教授、研究员、高级工程师及硕博士研究生，配备充足的高性能 GPU 计算资源，并为优秀团队成员提供赴国际顶尖高校开展学术交流与研究访问的机会。**团队长期面向海内外招收硕士、博士研究生及招聘博士后研究人员，优秀博士后综合年收入可达60万元，同时欢迎大二、大三本科生参与科研交流与实习。**
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

<style>
.profile.float-left {
  width: 25% !important;
  max-width: 220px !important;
  margin-right: 28px !important;
  margin-bottom: 10px !important;
}

.profile img {
  width: 100%;
  height: auto;
}

@media (max-width: 576px) {
  .profile.float-left {
    width: 40% !important;
    max-width: 180px !important;
    margin-right: 20px !important;
  }
}

article p {
  font-weight: 400 !important;
  line-height: 1.55;
}

/* Publication badges: PKU red, taller, larger text */
.publications .abbr .badge,
.publications .abbr abbr {
  #background-color: #8c1d40 !important;
  #color: #ffffff !important;
  #border-color: #8c1d40 !important;

  font-size: 1rem !important;
  font-weight: 700 !important;

  /* Increase height without changing width */
  padding-top: 0.5rem !important;
  padding-bottom: 0.5rem !important;
  line-height: 1.3 !important;

  border-radius: 6px !important;
  text-align: center !important;
  box-sizing: border-box;
}
</style>
