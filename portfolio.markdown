---
layout: page
title:  Portfolio
permalink: /portfolio/
---

This page serves as a portfolio/project collection page to show the different projects I have worked on.

## Ray Traced Reflections In Virtual Reality (Masters Thesis)
![Image](/img/master_thesis.png)

This project was developed together with [Lasse Korvig Bjerregaard](https://github.com/LasseKB) and [Daniel Gaard Hansen](https://github.com/Freemedude).
Code is publicly available here: [HybridVR](https://github.com/zfih/HybridVRThesis).

#### Abstract:
Good looking and immersive graphics is an important consideration when rendering true to life scenes.
Especially in Virtual Reality (VR), where the user is thrown into a virtual world replacing the real one.
One of the techniques for creating convincing virtual worlds is using ray tracing, which enables rendering high quality realistic effects such as reflections.
These effects, enabled by the introduction of DirectX Ray Tracing and the Nvidia RTX GPUs, have become another tool in the kit for real time rendering applica-tions.
However, since these effects are still computationally expensive, optimizations are required to reduce rendering times.

This thesis attempts to improve the quality of reflections typically found in video games, optimized for the demands of VR.
A total of five VR optimizations were implemented and had ray traced reflections integrated.
We extended an existing VR optimization, Accelerated Stereo Rendering by Wißmann et al. (2020), with two strategies for reusing reflections.
One strategy is to use the angle between the eyes towards the reflective surface, and the other the divergence of the reflected rays.
We named the prior strategy Incident Angle Pixel Conservation (IAPC) and the latter Ray Difference Pixel Conservation (RDPC).
Performance, user, image difference, and visual distinction tests were performed to evaluate the resulting solutions.
These results were also compared to the traditional rasterized Screen Space Reflec-tions technique.

The testing revealed that in the optimizations improve situations where alot of frame time was spent on ray tracing reflections.
When compared to a baseline which ray traces both eyes’ reflections in full resolution, the optimizations could reduce overall frame time by as much as 39% in IAPC and 21% in RDPC.
In addition to the performance difference between the two, the authors also find that artifacts introduced by RDPC make it a worse solution than IAPC.
Image difference tests show that the optimized reflections are not equivalent to the baseline version.
However, the user tests and visual distinction tests revealed that users have a hard time noticing slightly incorrect reflections in IAPC.
This means that even in scenes where reflections are rather clear and mirror like, our optimizations do not produce objectionable results in most situations.
In conclusion, this indicates that ouroptimization, IAPC, is worth considering in situations where reflections area major part of the frame budget.