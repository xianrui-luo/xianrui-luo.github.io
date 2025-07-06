---
title: "Dual-Camera All-in-Focus Neural Radiance Fields"
collection: publications
author: "Xianrui Luo, Zijin Wu, Juewen Peng, Huiqiang Sun, Zhiguo Cao, Guosheng Lin"
permalink: /publication/tpami25
# excerpt: '![](https://xianrui-luo.github.io/images/eccv2024.gif)'
excerpt: '<img src="https://xianrui-luo.github.io/images/pami.gif" width="60%" />'
date: 2025-04-01
venue: 'IEEE TPAMI'
codeurl: 'https://github.com/xianrui-luo/DCNeRF'
paperurl: 'https://ieeexplore.ieee.org/abstract/document/10858765/'
---

We present the first framework capable of synthesizing the all-in-focus neural radiance field (NeRF) from inputs without manual refocusing. Without refocusing, the camera will automatically focus on the fixed object for all views, and current NeRF methods typically using one camera fail due to the consistent defocus blur and a lack of sharp reference. To restore the all-in-focus NeRF, we introduce the dual-camera from smartphones, where the ultra-wide camera has a wider depth-of-field (DoF) and the main camera possesses a higher resolution. The dual camera pair saves the high-fidelity details from the main camera and uses the ultra-wide camera’s deep DoF as reference for all-in-focus restoration. To this end, we first implement spatial warping and color matching to align the dual camera, followed by a defocus-aware fusion module with learnable defocus parameters to predict a defocus map and fuse the aligned camera pair. We also build a multi-view dataset that includes image pairs of the main and ultra-wide cameras in a smartphone. Extensive experiments on this dataset verify that our solution, termed DC-NeRF, can produce high-quality all-in-focus novel views and compares favorably against strong baselines quantitatively and qualitatively. We further show DoF applications of DC-NeRF with adjustable blur intensity and focal plane, including refocusing and split diopter.