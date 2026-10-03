<div align="center">

# Liqing Tutorials

### 李庆个人教程合集

**Research workflows · Materials characterization · Scientific data analysis · AI for Research**

[![Tutorials](https://img.shields.io/badge/LQ%20Tutorials-001-2f6f5e?style=flat-square)](#tutorial-library)
[![Status](https://img.shields.io/badge/Status-Continuously%20Updated-6b7280?style=flat-square)](./CHANGELOG.md)
[![Language](https://img.shields.io/badge/Language-中文%20%7C%20English-b89b5e?style=flat-square)](#)
[![License](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-8b5e3c?style=flat-square)](./LICENSE.md)
[![GitHub](https://img.shields.io/badge/GitHub-liqinglq666-181717?style=flat-square&logo=github)](https://github.com/liqinglq666)

*Learn · Organize · Reproduce · Share*

</div>

---

## Quick Navigation

**[Featured Tutorial](#featured-tutorial)** ·
**[Tutorial Library](#tutorial-library)** ·
**[Knowledge Map](#knowledge-map)** ·
**[Future Releases](#future-releases)** ·
**[Tutorial Standard](#tutorial-standard)** ·
**[License & Reuse](#license--reuse)** ·
**[About Liqing](#about-liqing)**

---

## About this collection

**Liqing Tutorials** 是我长期维护的个人科研教程与实践笔记合集。

这里不追求“把所有知识都写一遍”，而是整理我在真实科研过程中反复使用、值得复现的操作流程、分析方法和工作习惯。内容主要围绕 **材料表征、科研数据分析、Scientific AI、科研工具与学术工作流** 展开。

> **Practical** — 以真实操作为主  
> **Reproducible** — 尽量给出清晰步骤与判断依据  
> **Research-oriented** — 服务于科研分析，而不是单纯的软件说明  
> **Versioned** — 每篇教程保留编号、版本和更新记录

---

## Featured Tutorial

<p align="center">
  <a href="./01-XRD/HighScore-Plus/">
    <img src="./assets/covers/LQ-Tutorial-001-cover.svg" width="880" alt="LQ Tutorial 001 · HighScore Plus XRD 操作教程">
  </a>
</p>

### LQ Tutorial 001 · HighScore Plus XRD 操作教程

**XRD Data Processing · Phase Identification · Rietveld Refinement**

从原始 XRD 数据导入开始，整理 HighScore Plus 日常分析与精修的完整主线：

`Open → Determine Background → Strip K-Alpha2 → Search Peaks → Peak Review → Search & Match → Phase Identification → Rietveld Refinement`

教程覆盖背景处理、Kα₂ 去除、自动寻峰与人工复查、物相检索、结构信息检查、SemiQuant、基准 Fit、Rwp / GOF 判断以及 Manual Refinement 等内容。

**Version:** v1.0 · 2026  
**Status:** ✅ Published

[**Read Tutorial Overview →**](./01-XRD/HighScore-Plus/) &nbsp; · &nbsp; [**View Full PDF →**](./01-XRD/HighScore-Plus/HighScore_Plus_XRD_Tutorial_Liqing_v1.0.pdf)

---

## Tutorial Library

| Series | Tutorial | Area | Version | Status |
| :---: | --- | --- | :---: | :---: |
| **001** | [**HighScore Plus XRD 操作教程**](./01-XRD/HighScore-Plus/) | Materials Characterization / XRD | v1.0 | ✅ Published |
| 002 | *LF-NMR 数据分析教程* | Materials Characterization / NMR | — | ◌ Planned |
| 003 | *DIC 裂缝分析教程* | Scientific Data Analysis / DIC | — | ◌ Planned |
| 004 | *科研绘图与图表整理教程* | Scientific Visualization | — | ◌ Planned |
| 005 | *SHAP 机器学习解释教程* | AI for Research | — | ◌ Planned |

> 新教程发布后会继续按照 **LQ Tutorial 00X** 的编号体系加入这里。

---

## Knowledge Map

| 🔬 **Materials Characterization** | 📊 **Scientific Data Analysis** |
| --- | --- |
| **XRD / HighScore Plus** — Published | Experimental data processing — Planned |
| LF-NMR — Planned | DIC / crack analysis — Planned |
| SEM / Microstructure — Planned | Visualization & reproducible analysis — Planned |
| Phase & pore structure analysis — Planned | Statistical & multivariate analysis — Planned |

| 🤖 **AI for Research** | ✍️ **Academic Workflow** |
| --- | --- |
| Machine learning for materials — Planned | Scientific writing — Planned |
| SHAP / model interpretation — Planned | Reviewer response — Planned |
| AI-assisted research workflow — Planned | Research figure workflow — Planned |
| Scientific computing tools — Planned | Reproducible documentation — Planned |

---

## Future Releases

The collection will expand gradually. Planned directions currently include:

- **LQ Tutorial 002 · LF-NMR 数据分析教程**  
  低场核磁数据处理、T₂ 分布读取、孔结构指标与结果表达。

- **LQ Tutorial 003 · DIC 裂缝分析教程**  
  DIC 数据处理、裂缝识别、裂缝宽度与应变场分析。

- **LQ Tutorial 004 · 科研绘图与图表整理教程**  
  科研图表的结构、版式、数据表达和可复现整理流程。

- **LQ Tutorial 005 · SHAP 机器学习解释教程**  
  面向科研数据的模型解释、SHAP 可视化与结果解读。

> “Planned” 仅代表后续整理方向，具体发布顺序会根据实际科研使用情况调整。

---

## Tutorial Standard

每篇教程尽量保持统一的“个人教程系列”格式：

```text
LQ Tutorial 00X
Title / 教程名称

Overview
Main Workflow
Detailed Steps
Key Parameters / Decision Rules
Common Problems
Version & Notes
Disclaimer
```

文件命名统一采用：

```text
Topic_Tutorial_Liqing_v1.0.pdf
```

后续更新通过版本号和 [CHANGELOG](./CHANGELOG.md) 记录。

---

## Repository Structure

```text
Liqing-Tutorials/
│
├── README.md
├── CHANGELOG.md
├── LICENSE.md
├── COPYRIGHT.md
├── TUTORIAL_TEMPLATE.md
├── assets/
│   └── covers/
│       └── LQ-Tutorial-001-cover.svg
│
└── 01-XRD/
    └── HighScore-Plus/
        ├── README.md
        └── HighScore_Plus_XRD_Tutorial_Liqing_v1.0.pdf
```

随着教程增加，会继续扩展分类，而不是为每篇教程单独建立一个仓库。

---

## License & Reuse

Original Liqing-created tutorial content in this repository is licensed under **Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)** unless otherwise stated.

In short:

- ✅ Personal study and non-commercial sharing
- ✅ Translation, adaptation and derivative tutorials
- ✅ Academic/laboratory redistribution with attribution
- **Attribution to Liqing / 李庆 is required**
- **Changes must be indicated**
- **Adapted material must remain ShareAlike**
- ❌ Commercial reuse is not granted without separate permission
- ⚠️ Third-party software interfaces, trademarks, database content and other third-party material are not relicensed by this repository

See **[LICENSE.md](./LICENSE.md)** for the repository license and **[COPYRIGHT.md](./COPYRIGHT.md)** for the detailed reuse and attribution rules.

> Recommended attribution: **Liqing / 李庆, _Liqing Tutorials_, [Tutorial Title], version [x.x], CC BY-NC-SA 4.0.**

---

## Notes & Disclaimer

This repository contains **independent educational notes and personal research workflows** compiled by Liqing.

Software names, interfaces, trademarks and proprietary database content belong to their respective owners. This repository does **not** distribute commercial software installers, license files, proprietary diffraction databases, or other restricted materials.

教程中的参数、流程和判断标准应结合具体仪器、软件版本、样品体系、实验室规范以及官方文档使用。

---

## About Liqing

**李庆 · Liqing**

Composite Materials · Scientific Computing · AI for Research · Data Analysis

[**GitHub Profile**](https://github.com/liqinglq666) · [**Tutorial Changelog**](./CHANGELOG.md)

---

<div align="center">

### Liqing Tutorials

**A growing personal knowledge base for research practice.**

<sub>Compiled, organized and maintained by Liqing.</sub>

</div>
