<div align="center">

# LQ Tutorial 001

## HighScore Plus XRD 操作教程

**XRD Data Processing · Phase Identification · Rietveld Refinement**

[![Series](https://img.shields.io/badge/LQ%20Tutorial-001-2f6f5e?style=flat-square)](../../)
[![Version](https://img.shields.io/badge/Version-v1.0-b89b5e?style=flat-square)](./HighScore_Plus_XRD_Tutorial_Liqing_v1.0.pdf)
[![Year](https://img.shields.io/badge/Year-2026-6b7280?style=flat-square)](#version--credits)
[![PDF](https://img.shields.io/badge/PDF-36%20pages-8b5e3c?style=flat-square)](./HighScore_Plus_XRD_Tutorial_Liqing_v1.0.pdf)

</div>

<p align="center">
  <a href="./HighScore_Plus_XRD_Tutorial_Liqing_v1.0.pdf">
    <img src="../../assets/covers/LQ-Tutorial-001-cover.svg" width="860" alt="LQ Tutorial 001 · HighScore Plus XRD 操作教程">
  </a>
</p>

<div align="center">

[**View Full PDF →**](./HighScore_Plus_XRD_Tutorial_Liqing_v1.0.pdf)
&nbsp; · &nbsp;
[**Back to Liqing Tutorials →**](../../)

</div>

---

## Quick Navigation

**[Overview](#overview)** ·
**[Main Workflow](#main-workflow)** ·
**[What It Covers](#what-it-covers)** ·
**[Refinement Logic](#refinement-logic)** ·
**[Key Notes](#key-notes)** ·
**[Version & Credits](#version--credits)**

---

## Overview

这是 **Liqing Tutorials / 李庆个人教程合集** 的第 001 篇教程。

本教程基于日常 XRD 数据处理与物相分析流程整理，覆盖从原始数据导入、背景处理、Kα₂ 去除、自动寻峰与人工复查，到 Search & Match、候选物相核对、SemiQuant 预览、Rietveld Fit 与进一步精修的完整操作链。

它更偏向 **“真实操作流程 + 判断依据 + 返工逻辑”**，而不是单纯的软件菜单说明。

---

## Main Workflow

```text
Open raw XRD data
        ↓
Determine Background
        ↓
Strip K-Alpha2
        ↓
Search Peaks
        ↓
Peak List Review
        ↓
Search & Match
        ↓
Check candidate phases
        ↓
Accept Candidate
        ↓
SemiQuant / Quantification Preview
        ↓
Save preFit.HPF
        ↓
Initial Fit
        ↓
Check curve + residual + Rwp / GOF
        ↓
Manual Refinement (if needed)
        ↓
Final Quantification
```

> **Core sequence:** `Determine Background → Strip K-Alpha2 → Search Peaks`  
> Kα₂ 去除在寻峰之前完成，避免重复峰或肩峰干扰后续峰表判断。

---

## What It Covers

### 01 · Data Preparation

- XRD 原始数据导入与图谱完整性检查
- File / Treatment / Analysis / Customize 等常用入口
- 原始文件备份与工程文件管理

### 02 · Background & Peak Processing

- Determine Background
- Granularity / Bending factor 的作用
- `More >>` 中最低峰值强度阈值
- Strip K-Alpha2
- Search Peaks
- Minimum significance、tip width、peak base width
- Peak List 人工补峰 / 删峰

### 03 · Peak Information

- Position (2θ)
- Height
- FWHM
- Area
- d-spacing
- Relative Intensity
- Background
- Significance
- Matched / Matched by
- Crystallographic Properties：h、k、l、F observed / F calculated

### 04 · Phase Identification

- Search & Match
- Restriction set
- Chemistry restrictions
- Periodic Table 元素限制
- Candidates / Selected Candidate
- Accepted Ref. Pattern
- 参考峰、实验峰和材料体系的综合判断

### 05 · Structure Information

- ICDD / PDF 参考卡片的使用边界
- CIF / COD / ICSD 结构信息检查
- Rietveld 定量前确认晶体结构模型
- C-S-H 等低结晶 / 无定形相的处理提醒

### 06 · Quantification & Fit

- SemiQuant / Quantification 预览
- Fit 前另存 `preFit.HPF`
- Accepted Ref. Pattern 全选
- Automatic / Default 基准拟合
- 实验曲线与计算曲线
- Difference / Residual
- Rwp / GOF

---

## Refinement Logic

教程中的进一步精修遵循：

```text
Initial Automatic Fit
        ↓
Check residual + Rwp / GOF
        ↓
Manual Mode
        ↓
Global terms
        ↓
Major phases
        ↓
Minor phases
        ↓
Re-check physical reasonableness
```

### ① Global terms

优先判断是否存在全谱统一峰位偏移，再考虑：

- Zero Shift [2Theta]
- Specimen Displacement [mm]

这两类参数都可能造成整体峰位移动，因此通常不建议同时释放。

### ② Major phases

按需要逐步检查：

```text
Scale Factor
    ↓
Preferred Orientation
    ↓
Phase Profile / Profile Fitting
    ↓
Unit Cell
```

其中峰形参数按照残差逐组开启，常见操作包括：

- U / V / W
- Shape 1 / Shape 2 / Shape 3
- S/L Asymmetry
- D/L Asymmetry

### ③ Minor phases

微量相只有在具有足够独立特征峰、残差确实指向该相时，再逐步增加自由参数，避免通过异常峰宽、晶胞或取向参数“吸收”其他误差。

> **操作逻辑：** `勾选 Refine → 运行 Fit → 检查结果 → 再决定下一组参数`  
> 而不是手动猜数值或一次性 Refine All。

---

## Key Notes

### Background

- Bending factor 不宜过大，避免背景线过度弯曲并“吃掉”弱峰或宽峰。
- 常规水泥基样品可从中等偏小的 Bending factor 开始，再结合当前图谱调整。
- `More >>` 中 Intensity [cts] 可从约 **500 cts** 作为初始参考，再根据信噪比和弱峰情况调整。

### Phase Identification

候选物相不能只看软件 Score。应同时核对：

- 主要峰位是否对应
- 强特征峰是否存在
- 候选卡片是否引入实验中不存在的强峰
- 物相是否符合原料组成、龄期与养护条件

### Rietveld Fit

本教程采用的经验参考为：

- **Rwp < 10%**
- **GOF < 2**

但这两个指标不能单独决定拟合是否可靠，还需要同时检查：

- 实验曲线与计算曲线的重合
- Difference / Residual 是否存在系统偏差
- 物相组合是否合理
- 参数是否出现异常漂移或卡边界
- 结构模型与实际晶型 / 水化状态是否匹配

---

## Full Tutorial

### 📘 HighScore Plus XRD 操作教程 · v1.0

[**Open the complete 36-page PDF →**](./HighScore_Plus_XRD_Tutorial_Liqing_v1.0.pdf)

PDF 中包含完整步骤、软件界面截图、操作标注、拟合返工逻辑以及常见水泥基材料 XRD 物相参考内容。

---

## Version & Credits

| Item | Information |
| --- | --- |
| Series | **LQ Tutorial 001** |
| Title | **HighScore Plus XRD 操作教程** |
| Subtitle | XRD Data Processing · Phase Identification · Rietveld Refinement |
| Version | **v1.0** |
| Year | **2026** |
| Compiled by | **李庆 Liqing** |
| Institution | Sun Yat-sen University |
| Lab | Advanced Green Geo-Materials Lab |
| Collection | [Liqing Tutorials](../../) |

---

## Notes & Disclaimer

本教程属于个人学习、科研实践与实验室日常流程的整理版本。不同仪器、HighScore Plus 版本、数据库配置、样品体系与实验室规范可能导致参数入口、默认值或适用设置存在差异。

This is an independent educational tutorial and is not affiliated with or endorsed by the software vendor.

HighScore Plus and related software interfaces, trademarks and proprietary database content belong to their respective owners. Commercial software installers, license files and proprietary database packages are not distributed in this repository.

Original tutorial text, annotations, workflow summaries and organization are compiled by **Liqing**.

### License

Unless otherwise stated, original Liqing-created content in this tutorial is licensed under **CC BY-NC-SA 4.0**. Attribution is required; non-commercial sharing and adaptation are permitted; adaptations must indicate changes and remain ShareAlike.

Third-party software interfaces, trademarks, database content, and other third-party material shown or referenced in this tutorial are excluded from this license and remain subject to their respective rights.

See the repository-wide [LICENSE.md](../../LICENSE.md).

---

<div align="center">

### LQ Tutorial 001

**From raw XRD data to interpretable refinement results.**

[**← Liqing Tutorials**](../../) &nbsp; · &nbsp; [**Full PDF →**](./HighScore_Plus_XRD_Tutorial_Liqing_v1.0.pdf)

</div>
