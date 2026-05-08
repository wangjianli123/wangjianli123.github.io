---
layout: single
title: ""
permalink: /
author_profile: true
---
<style>
@media (min-width: 1024px) {

  .sidebar {
    float: left !important;
    width: 180px !important;
    margin-left: 0 !important;
    padding-right: 10px !important;
  }

  .page {
    float: left !important;
    width: calc(100% - 200px) !important;
    margin-left: 0 !important;
    padding-left: 20px !important;
    padding-right: 0 !important;
  }

  .page__inner-wrap,
  .page__content {
    max-width: none !important;
  }

}
</style>
## About Me {#about}

I am currently working with the [School of Computing and Artificial Intelligence](https://scai.swjtu.edu.cn/index.html), [Southwest Jiaotong University](https://www.swjtu.edu.cn), Chengdu, China. I received the Ph.D. degree (advised by [Ting-Zhu Huang](https://www.math.uestc.edu.cn/info/1183/5808.htm)) from the [School of Mathematical Sciences](https://www.math.uestc.edu.cn/), [University of Electronic Science and Technology of China](https://www.uestc.edu.cn), Chengdu, China, in 2022.

My current research interests include tensor modeling and computing, high-dimensional image processing, computer vision, and deep learning.

📢 **My group recruits 1–2 PhD students and 7–10 Master's students each year. Undergraduate students interested in gaining hands-on research experience are also welcome to join our research training program. I especially encourage self-motivated students to reach out. Please feel free to contact me!**

📧 E-mail: wangjianli_123@163.com, wangjianli@swjtu.edu.cn &emsp; 🎓 [Google Scholar](https://scholar.google.com/citations?hl=en&user=6QVFljgAAAAJ) &emsp; 🏫 [Faculty Homepage](https://faculty.swjtu.edu.cn/wangjianli/zh_CN/)

## News {#news}

- 2024.7.1: Two papers have been accepted by **European Conference on Computer Vision (ECCV) 2024**.
- 2024.1.11: One paper "Snapshot Compressive Imaging Using Domain-Factorized Deep Video Prior" has been accepted by **IEEE Transactions on Computational Imaging**.
- 2023.7.11: One paper "Unsupervised Domain Factorization Network for Thick Cloud Removal of Multi-temporal Remotely Sensed Images" has been accepted by **IEEE Transactions on Geoscience and Remote Sensing**.

## Publications {#publications}

{% include base_path %}

{% assign current_year = "" %}
{% assign pubs = site.publications | sort: "date" | reverse %}

{% for post in pubs %}
{% assign post_year = post.date | date: "%Y" %}
{% if post_year != current_year %}
<h2>{{ post_year }}</h2>
{% assign current_year = post_year %}
{% endif %}

{% include archive-single-publication.html %}
{% endfor %}

## Services {#services}

- IEEE Transactions on Image Processing (IEEE TIP), Reviewer
- IEEE Transactions on Neural Networks and Learning Systems (IEEE TNNLS), Reviewer
- IEEE Transactions on Geoscience and Remote Sensing (IEEE TGRS), Reviewer
- IEEE Transactions on Circuits and Systems for Video Technology (IEEE TCSVT), Reviewer
- IEEE Transactions on Computational Imaging (IEEE TCI), Reviewer

## Fundings {#fundings}


- 国家自然科学基金青年项目, 2024.01-2026.12
- 四川省自然科学基金青年项目, 2023.01-2024.12
- 国家资助博士后研究人员计划, 2024.01-2025.12
- 数据恢复四川省重点实验室开放课题重点项目, 2024.06-2026.06
- 中央高校基本科研业务项目, 2023.01-2024.12

## activities
- 10/2021: "Multi-Dimensional Visual Data Completion via Low-Rank Tensor Representation Under Coupled Transform", CSIAM 2021, **Anhui, China**, [[Slide]](../images/IGRASS2021_1400.pdf)
- 07/2021: "Hyperspectral Denoising Via Global Tensor Ring Decomposition and Local Unsupervised Deep Image Prior", IGARSS 2021, **Online**, [[Slide]](../images/IGRASS2021_1400.pdf)
