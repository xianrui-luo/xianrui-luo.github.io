---
title: "Dynamic Neural Radiance Field From Defocused Monocular Video"
collection: publications
author: "Xianrui Luo, Huiqiang Sun, Juewen Peng, Zhiguo Cao"
permalink: /publication/eccv24
# excerpt: '![](https://xianrui-luo.github.io/images/eccv2024.gif)'
# excerpt: '<img src="https://xianrui-luo.github.io/images/eccv2024.gif" width="60%" />'
excerpt: '<video autoplay loop muted playsinline width="60%"><source src="https://xianrui-luo.github.io/images/eccv2024.mp4" type="video/mp4"></video>'
date: 2024-07-01
venue: 'ECCV'
codeurl: 'https://github.com/xianrui-luo/D2RF'
paperurl: 'https://arxiv.org/abs/2407.05586'
---

Dynamic Neural Radiance Field (NeRF) from monocular videos has recently been explored for space-time novel view synthesis and achieved excellent results. However, defocus blur caused by depth variation often occurs in video capture, compromising the quality of dynamic reconstruction because the lack of sharp details interferes with modeling temporal consistency between input views. To tackle this issue, we propose D2RF, the first dynamic NeRF method designed to restore
sharp novel views from defocused monocular videos. We introduce layered Depth-of-Field (DoF) volume rendering to model the defocus blur and reconstruct a sharp NeRF supervised by defocused views. The blur model is inspired by the connection between DoF rendering and volume rendering. The opacity in volume rendering aligns with the layer visibility in DoF rendering. To execute the blurring, we modify the layered blur kernel to the ray-based kernel and employ an optimized sparse kernel
to gather the input rays efficiently and render the optimized rays with our layered DoF volume rendering. We synthesize a dataset with defocused dynamic scenes for our task, and extensive experiments on our dataset show that our method outperforms existing approaches in synthesizing all-in-focus novel views from defocus blur while maintaining spatial-temporal consistency in the scene.
