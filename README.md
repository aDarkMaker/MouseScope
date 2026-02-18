# 🐭 MouseScope Desktop

<p align="center">
  <img src="static/img/logo.png" alt="MouseScope Logo" width="160" onerror="this.style.display='none'"/>
</p>

<p align="center">
  <b>Automated Mouse Tail Suspension Test (TST) Analysis Software</b><br>
  小鼠悬尾实验自动化分析软件
</p>

<p align="center">
  <img src="https://img.shields.io/badge/license-Non--Commercial%20Academic-blue" alt="License"/>
  <img src="https://img.shields.io/badge/platform-Windows-lightgrey" alt="Platform"/>
  <img src="https://img.shields.io/badge/python-3.9%2B-green" alt="Python"/>
  <img src="https://img.shields.io/badge/version-1.0-orange" alt="Version"/>
</p>

---

## 📖 Overview | 项目简介

**MouseScope** is a fully automated analysis tool for the **Mouse Tail Suspension Test (TST)**, a widely used behavioral assay in neuroscience research to evaluate depression-like phenotypes.

**MouseScope** 是一款专为小鼠悬尾实验（TST）设计的全自动化分析工具，用于神经科学研究中抑郁样行为表型的评估。

**Key Features | 核心功能：**

- 🎯 **Automated Immobility Detection** — Computer vision-based tracking, no manual scoring
  全自动不动性检测，无需人工评分
- 📹 **Video Upload & Processing** — Supports common video formats (MP4, AVI, MOV)
  支持主流视频格式上传与批量处理
- 🔲 **Interactive ROI Calibration** — Flexible Region of Interest selection
  可交互的感兴趣区域（ROI）标定
- 📊 **Multi-format Output** — CSV data tables + detailed analysis reports
  多格式输出：CSV 数据表 + 详细分析报告
- 🖥️ **Desktop GUI** — Browser-based interface, no coding required
  基于浏览器的桌面 GUI，零代码门槛
- ⚡ **High Performance** — Multi-core CPU optimization, optional OpenCV CUDA acceleration
  多核 CPU 优化，可选 OpenCV CUDA 加速

---

## 🛠️ Technical Stack | 技术栈

| Component | Technology |
|-----------|-----------|
| Backend | Python 3.9+, Flask |
| Computer Vision | OpenCV, Optical Flow, Background Subtraction |
| Optional AI | YOLOv11-seg (Ultralytics) |
| Data Processing | NumPy, Pandas |
| Frontend | HTML5, CSS3, Vanilla JS |
| Packaging | PyInstaller (Windows EXE) |

**Algorithm Pipeline | 算法流程：**

```
Video Input → ROI Calibration → Background Subtraction
    → Morphological Processing → Mouse Detection
    → Optical Flow Analysis → Immobility Classification
    → Report Generation (CSV + TXT)
```

---

## 🚀 Quick Start | 快速上手

### Option 1: Pre-built EXE (Windows) | 方式一：直接使用 EXE

1. Download `MouseScope.zip` from [Releases](../../releases)
2. Extract and double-click `MouseScope.exe`
3. Browser opens automatically at `http://localhost:8080`

### Option 2: Run from Source | 方式二：从源码运行

```bash
# Clone the repository
git clone https://github.com/YourUsername/MouseScope.git
cd MouseScope

# Install dependencies
pip install -r requirements.txt

# Run
python app.py
```

Then open `http://localhost:8080` in your browser.


---

## 📋 Usage Workflow | 使用流程

```
1. Upload Video     →  上传实验视频（MP4 / AVI / MOV）
2. Calibrate ROI    →  框选单只小鼠区域
3. Start Analysis   →  自动运行 CV 分析
4. Download Report  →  下载 CSV + 分析报告
```

### Output Files | 输出文件

| File | Content |
|------|---------|
| `*_logs.csv` | Frame-by-frame tracking data 逐帧追踪数据 |
| `*_immobility.csv` | Immobility statistics 不动性统计 |
| `*_report.txt` | Full analysis report 完整分析报告 |

---

## 📐 System Requirements | 系统要求

- **OS**: Windows 10 / 11 (x64)
- **RAM**: ≥ 8 GB recommended
- **CPU**: Multi-core (4+ cores recommended for real-time analysis)
- **Storage**: ≥ 500 MB free space
- **Python**: 3.9 – 3.11 (for source mode)

---

## 📚 Citation | 引用说明

If you use MouseScope Desktop in your research, **please cite**:

如果您在研究中使用了本软件，**请务必引用**：

```bibtex
@software{fu2026mousescope,
  author  = {Fu, Jiacheng (付家丞)},
  title   = {MouseScope Desktop: Automated Mouse Tail Suspension Test Analysis Software},
  year    = {2026},
  url     = {https://github.com/YourUsername/MouseScope},
  version = {1.0}
}
```

**Plain text format | 纯文本格式：**

> Fu, J. (2026). *MouseScope Desktop: Automated mouse tail suspension test analysis software* (Version 1.0) [Software]. GitHub. https://github.com/YourUsername/MouseScope

---

## ⚖️ License | 许可证

This software is **free for academic and non-commercial use only**.

本软件**仅供学术研究和非商业用途免费使用**。

| Use Case | Allowed |
|----------|---------|
| Academic research 学术研究 | ✅ Free |
| Educational use 教学使用 | ✅ Free |
| Publication (with citation) 发表论文（需引用） | ✅ Free |
| Commercial use 商业使用 | ❌ Contact author |
| Enterprise internal use 企业内部使用 | ❌ Contact author |
| CRO / pharma companies CRO/制药公司 | ❌ Contact author |

For commercial licensing, please contact the author.
如需商业授权，请联系作者。

See [LICENSE](LICENSE) for full terms.

---

## 📬 Contact | 联系方式

**Author | 作者**: 付家丞 (Jiacheng Fu)

**Email**: 2583348593@qq.com

**For commercial licensing | 商业合作**: Please email with subject line `[MouseScope Commercial License]`

---

## 🙏 Acknowledgements | 致谢

Built with:
- [OpenCV](https://opencv.org/) — Computer vision library
- [Flask](https://flask.palletsprojects.com/) — Web framework
- [Ultralytics YOLOv11](https://github.com/ultralytics/ultralytics) — Optional AI backbone

---

<p align="center">
  Made with ❤️ for the neuroscience research community<br>
  为神经科学研究社区用心打造
</p>
