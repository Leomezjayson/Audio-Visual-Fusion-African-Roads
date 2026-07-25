# NOTICE — Intellectual Property & Usage Terms

**Project:** SenseAI Research — Audio-Visual Fusion for African Road Safety  
**Author:** Miguel Oppong Ligi
**University:** Ghana Communication Technology University 
**Last Updated:** 2026

---

## 📌 Overview

This repository contains research code for my undergraduate thesis. The project is a **mixed-license** repository. 

- **Open-source components** are freely available for academic and non-commercial use.
- **Proprietary components** (model weights, dataset) are reserved for commercial use and are **not** open-sourced.

**Please read this notice carefully before using any part of this repository.**

---

## 🆓 Open-Source Components (MIT License)

The following components are released under the **MIT License** and are freely available for academic, research, and non-commercial use:

| Component | What It Includes |
| :--- | :--- |
| **Code Framework** | All Python scripts (`src/`), data loaders, training pipelines, evaluation scripts |
| **Notebooks** | Jupyter notebooks for data exploration and baseline experiments (`notebooks/`) |
| **Configuration Files** | YAML configuration files (`configs/`) |
| **Documentation** | README.md, CONTRIBUTING.md, and all Markdown documentation |
| **Baseline Models** | Implementation of vision encoders (ResNet50, YOLOv8) and audio encoders (VGGish, Transformers) |

### ✅ What You Can Do:
- Use, modify, and distribute the open-source code for academic research
- Cite the work in your publications
- Contribute improvements via Pull Requests
- Fork the repository for your own research

### ❌ What You Cannot Do:
- Use the open-source code for **commercial purposes** without explicit written permission
- Claim the code as your own original work
- Remove or modify this NOTICE file

---

## 🔒 Proprietary Components (All Rights Reserved)

The following components are **NOT** open-sourced and remain the exclusive intellectual property of [Your Full Name] / SenseAI:

| Component | What It Includes | Why It's Protected |
| :--- | :--- | :--- |
| **Trained Model Weights** | `.pt`, `.pth`, `.onnx` files from training | Core IP; the "secret sauce" of the fusion mechanism |
| **Full Dataset** | Raw video/audio recordings and annotations | Data moat; NVIDIA/Meta cannot replicate African road data |
| **Proprietary Fusion Module** | Novel dynamic fusion algorithm implementation | Patentable innovation; commercial advantage |
| **Deployment Code** | Code that packages the model for edge devices | Commercial product pipeline |
| **Business Logic** | Pricing models, customer insights, market data | Competitive advantage |

### ❌ What You Cannot Do:
- Download, reproduce, or use the proprietary components for any purpose
- Reverse-engineer the trained models
- Distribute the dataset or any derivative of it
- Use the proprietary components in commercial products

### 📧 For Commercial Use:
If you are interested in licensing the proprietary components, please contact:

- **Author:** Miguel Oppong Ligi
- **Email:** 1703240434@live.gctu.edu.gh
- **Purpose:** Commercial licensing inquiries

---

## 📊 Dataset Usage Policy

Our African Road Dataset (ARD) is **proprietary** and **not publicly available** in its full form.

| Dataset Version | Availability | Usage |
| :--- | :--- | :--- |
| **Full Dataset** | ❌ Private | Reserved for thesis and startup commercial use |
| **Sample Dataset** | ✅ Planned | 5-hour sample will be released upon thesis completion for reproducibility |

**Release Date (Sample Dataset):** [Month, Year] (upon thesis submission)

---

## 📝 Academic Citation

If you use the open-source code or reference this research in your work, please cite:

```bibtex
@thesis{[YourLastName]2026,
  author = {Miguel Oppong Ligi},
  title = {Dynamic Audio-Visual Fusion for Proactive Collision Avoidance in Unstructured Traffic Environments},
  school = {Ghana Communication Technology University},
  year = {2026},
  address = {Accra, Ghana},
  url = https://github.com/Leomezjayson/Audio-Visual-Fusion-African-Roads/
}
🤝 Contributing

We welcome contributions to the open-source components of this repository. By contributing, you agree that:

1. Your contributions will be licensed under the MIT License
2. You assign copyright of your contributions to the project author for licensing purposes
3. You will not contribute proprietary code or data

See CONTRIBUTING.md for detailed guidelines.

---

⚖️ Governing Law

The laws of Ghana govern this notice and the intellectual property described herein. Any disputes shall be resolved in the courts of Ghana.

---

📬 Contact for IP Inquiries

For any questions regarding licensing, usage rights, or partnership opportunities:

· Name: Miguel Oppong Ligi
· Email: [Your University Email]
· LinkedIn: [Your LinkedIn URL]
· GitHub: [Your GitHub Profile]

---

© 2026 Miguel Oppong Ligi. All Rights Reserved.

This file is part of the SenseAI Research repository and may not be removed or altered without permission.
