<div align="center">

# AlayaCrafter: An Open-Source 3D Foundation Stack for AI-Native Games

[Yonghao Yu](https://scholar.google.com/citations?user=lwuwuAYAAAAJ) · [Ruihan Yu](https://auroraryan0301.github.io/) · [Sho Kuno](https://shokuno5.github.io/) · [Muyao Niu](https://myniuuu.github.io/) · [Yu-Ju Tsai](https://liagm.github.io/) · [Zheng-Hui Huang](https://brian90709.github.io/) · [Chuanhao Li](https://nevermorelch.github.io/) · [Fengbo Lan](https://openreview.net/profile?id=%7EFengbo_Lan1) · [Runyi Li](https://lirunyi2001.github.io/)

[Ming-Hsuan Yang](https://faculty.ucmerced.edu/mhyang/) · [Kaipeng Zhang](https://kpzhang93.github.io/)<sup>†</sup> · [Zhixiang Wang](https://lightchaserx.github.io/)<sup>†</sup>

<sup>†</sup> Corresponding authors


**[AlayaLab](https://github.com/AlayaLab)**

[![Project Page](https://img.shields.io/badge/Project-Page-1683D8)](https://alaya-lab.github.io/AlayaCrafter/)
[![3D Asset Library](https://img.shields.io/badge/3D-Asset%20Library-5B6EE1)](https://alaya-lab.github.io/AlayaCrafter/space-kit.html)

**Compact meshes. Explicit topology. Editable worlds.**

</div>

## Overview

AlayaCrafter brings compact, editable 3D assets into an explicit scene state for AI-native game engines. **AlayaCrafter-Base** turns a single image into a native triangle mesh with a controllable face budget. Programs and agents can inspect these meshes, assemble them into scenes, and author their motion.

This is the official repository for the AlayaCrafter model and workflow. The project website and interactive asset library are available now; code, model weights and the paper are planned for release here.

## Designed for Agent-Efficient 3D Authoring

AI-native engines need a 3D state that their simulation, controllers and agents can read and edit. Compact geometry and explicit triangle connectivity give agents concrete objects to work with. Geometry, transforms, cameras and motion remain accessible throughout scene construction and revision.

AlayaCrafter-Base generates vertices coarse to fine with a diffusion transformer over a sparse octree, then predicts connectivity with a second diffusion transformer in the latent space of a topology autoencoder. A face budget controls mesh complexity.

## From Meshes to Worlds

The authoring workflow carries generated geometry into ordinary 3D tools:

1. **Generate meshes:** create compact geometry with explicit vertices and triangle faces.
2. **Assemble scenes:** arrange assets and parts in an editable 3D scene.
3. **Author materials and motion:** add UVs, materials, rigs, part transforms and animation.
4. **Render the scene:** define cameras, lighting and effects to produce geometry and material control videos.

A video-generation model can use a control video as a soft condition for an additional appearance stage. The base model generates mesh geometry and connectivity; UVs, materials, rigs, scene assembly and choreography belong to the authoring workflow.

## Explore Space Saga

**[Space Saga](https://alaya-lab.github.io/AlayaCrafter/#saga)** showcases twelve scenes built from the space asset kit, including stations, fleets, shipyards, moon bases and alien encounters. Compare **Materials** with **Gray mesh** or **Topology** on the same scene timeline.

All twelve scenes use AlayaCrafter generated meshes with their original topology.

The **[3D asset library](https://alaya-lab.github.io/AlayaCrafter/space-kit.html)** contains **123 assets**, with input-image, gray-mesh, topology and material views, interactive 3D inspection and original GLB downloads. Explore modular assemblies and scenes built from the kit, with **Materials**, **Gray mesh** and **Topology** comparisons.

## Release Status

- [x] Project website and Space Saga showcase
- [x] Interactive 3D asset library and asset downloads
- [ ] AlayaCrafter-Base code
- [ ] Model weights
- [ ] AlayaCrafter workflow and tools
- [ ] Paper and workflow documentation

Installation instructions, model download links and paper details will be added here as each release becomes available.
