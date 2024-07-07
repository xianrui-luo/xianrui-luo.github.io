---
title: "Point-and-Shoot All-in-Focus Photo Synthesis From Smartphone Camera Pair"
collection: publications
author: "Xianrui Luo, Juewen Peng, Weiyue Zhao, Ke Xian, Hao Lu, Zhiguo Cao"
permalink: /publication/TCSVT
excerpt: '![](https://xianrui-luo.github.io/images/tcsvt.jpg)'
date: 2022-11-01
venue: 'TCSVT'
codeurl: 'http://academicpages.github.io/files/slides3.pdf'
paperurl: 'https://ieeexplore.ieee.org/abstract/document/9953190'
---

All-in-Focus (AIF) photography is expected to be a commercial selling point for modern smartphones. Standard AIF synthesis requires manual, time-consuming operations such as focal stack compositing, which is unfriendly to ordinary people. To achieve point-and-shoot AIF photography with a smartphone, we expect that an AIF photo can be generated from one shot of the scene, instead of from multiple photos captured by the same camera. Benefiting from the multi-camera module in modern smartphones, we introduce a new task of AIF synthesis from main (wide) and ultra-wide cameras. The goal is to recover sharp details from defocused regions in the main-camera photo with the help of the ultra-wide-camera one. The camera setting poses new challenges such as parallax-induced occlusions and inconsistent color between cameras. To overcome the challenges, we introduce a predict-and-refine network to mitigate occlusions and propose dynamic frequency-domain alignment for color correction. To enable effective training and evaluation, we also build an AIF dataset with 2686 unique scenes. Each scene includes two photos captured by the main camera, one photo captured by the ultra-wide camera, and a synthesized AIF photo. Results show that our solution, termed EasyAIF, can produce high-quality AIF photos and outperforms strong baselines quantitatively and qualitatively. For the first time, we demonstrate point-and-shoot AIF photo synthesis successfully from main and ultra-wide cameras.
