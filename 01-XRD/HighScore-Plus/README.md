# LQ Tutorial 001 · HighScore Plus XRD 操作教程

> **XRD Data Processing · Phase Identification · Rietveld Refinement**

这是 **Liqing Tutorials / 李庆个人教程合集** 的第 001 篇教程。

---

## Tutorial Overview

本教程围绕 HighScore Plus 的日常 XRD 数据处理流程整理，覆盖从原始数据导入、背景处理、Kα₂ 去除、自动寻峰与人工复查，到 Search & Match、物相确认、SemiQuant 预览以及 Rietveld refinement 的完整工作流。

### Main Workflow

```text
Open
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
Accept Candidate
  ↓
SemiQuant / Quantification Preview
  ↓
Initial Fit
  ↓
Rietveld Refinement
  ↓
Residual + Rwp / GOF + Physical Reasonableness
```

---

## Contents

- XRD 原始数据导入与检查
- Determine Background
- Strip K-Alpha2
- Search Peaks
- Peak List 人工补峰 / 删峰
- Object Inspector 峰信息
- Search & Match
- Restriction set 与 Chemistry 限制
- 候选物相与参考卡片核对
- CIF / COD / ICSD 结构信息检查
- Accepted Ref. Pattern
- SemiQuant / Quantification
- Fit 前保存与基准拟合
- Rwp / GOF 与残差判断
- Manual Refinement Control
- Zero Shift / Specimen Displacement
- Scale Factor
- Preferred Orientation
- U / V / W / Shape / Asymmetry
- Unit Cell
- 微量相精修与返工逻辑

---

## Full PDF

📘 **PDF:** [HighScore_Plus_XRD_Tutorial_Liqing_v1.0.pdf](./HighScore_Plus_XRD_Tutorial_Liqing_v1.0.pdf)

> 如果当前链接暂时不可用，说明 PDF 文件尚未上传到本目录。

---

## Version

| Item | Information |
| --- | --- |
| Series | **LQ Tutorial 001** |
| Title | HighScore Plus XRD 操作教程 |
| Version | **v1.0** |
| Year | **2026** |
| Compiled by | **李庆 Liqing** |
| Institution | Sun Yat-sen University |
| Lab | Advanced Green Geo-Materials Lab |

---

## Notes

本教程属于个人学习、科研实践与组内工作流程的整理版本。不同仪器、HighScore Plus 版本、数据库配置、样品体系与实验室规范可能导致参数入口或推荐设置存在差异。

特别是 Rietveld refinement，不建议仅追求更低的 Rwp / GOF；还应同时检查实验曲线与计算曲线、残差、结构模型、参数变化及物理合理性。

---

## Copyright & Disclaimer

This is an independent educational tutorial and is not affiliated with or endorsed by the software vendor.

HighScore Plus and related software interfaces, trademarks and proprietary database content belong to their respective owners. Commercial software installers, license files and proprietary database packages are not distributed in this repository.

Original tutorial text, annotations, workflow summaries and personal organization are compiled by **Liqing**.

---

← [Back to Liqing Tutorials](../../)
