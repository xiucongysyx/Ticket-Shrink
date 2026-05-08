<div align="center">

# 🎫 Ticket-Shrink

**一个极其轻量的电子发票/客票紧凑排版工具**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Pure Frontend](https://img.shields.io/badge/Tech-Pure_HTML/JS-f39f37.svg)](#)
[![Privacy First](https://img.shields.io/badge/Privacy-100%25_Local-4caf50.svg)](#)

[在线体验 (GitHub Pages)](您的GitHub_Pages链接) · [报告 Bug](您的Issues链接) · [提出建议](您的Issues链接)

</div>

---

## 💡 简介 (About)

现代高铁电子发票为了适配 A4 纸张，排版通常极为松散。当你想要将它们打印成 **传统火车票大小 (8.56cm x 5.4cm)** 放入卡包或作为手账素材收集时，直接缩小会导致文字糊成一团，难以辨认。

**Ticket-Shrink** 是一个纯前端实现的无损重组工具。它不需要配置任何复杂的 Python 或后端环境，只需双击打开网页，即可通过算法将松散的元素“挤压”在一起，生成极致紧凑的卡片版式。

## ✨ 核心特性 (Features)

- 🛡️ **绝对的隐私安全：** 纯本地浏览器 Canvas 运算，**无任何图片上传或服务器交互**，保护您的身份信息与出行隐私。
- ✂️ **无损切片折叠 (Seam Carving)：** 摒弃粗暴的图像缩放。算法基于像素边缘探测，像折纸一样折叠空白区域，**100% 保证文字比例不失真、不被压扁**。
- 🥞 **智能分层处理：** 将主体文字区与底部的“虚线说明框”剥离，支持分别独立控制 X 轴与 Y 轴的压缩率。
- 📏 **精准卡片比例：** 一键自动补齐底色至 `8.56 : 5.4` 标准卡片比例，右键保存后即可直接按 100% 比例打印，告别手动裁切。
- 🚀 **开箱即用：** 零依赖，单文件，双击 `index.html` 即可运行。

## 📸 效果演示 (Demo)

*(请在此处替换为你的实际效果图)*

| 处理前 (原始 A4 比例电子票) | 处理后 (标准卡片比例紧凑版) |
| :---: | :---: |
| <img src="assets/before-demo.jpg" width="400"> | <img src="assets/after-demo.jpg" width="400"> |

## 🚀 快速开始 (Usage)

由于本项目采用纯前端单文件架构，无需任何安装步骤：

1. 克隆或下载本仓库到本地。
2. 使用任何主流浏览器（Chrome, Edge, Safari 等）双击打开 `index.html`。
3. 点击 **“选择发票图片”**，载入您的电子客票。
4. 拖动面板上的三个核心滑块，实时预览排版效果：
   - **主体纵向行距 (Y轴)**
   - **主体横向间距 (X轴)**
   - **底部虚线框长度 (X轴)**
5. 调整至满意后，在右侧生成的图片上 **右键 -> 图片另存为** 即可。

## 🛠️ 技术细节与局限性 (Technical Details & Limitations)

本项目采用**非 OCR** 的纯视觉像素扫描方案（基于灰度对比度的智能留白消除）。
- **优势：** 运行极快，跨平台，无需加载几十 MB 的字库或识别模型。
- **局限性：** 算法依赖于标准电子发票的留白特征。如果发票截图带有严重噪点、水印，或者不同地区的排版存在巨大结构差异，可能会导致切片误判。

## 🤝 贡献 (Contributing)

发现排版 Bug 或者有更好的 Canvas 处理算法？非常欢迎提交 Pull Request！

1. Fork 本仓库
2. 创建您的特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交您的更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启一个 Pull Request

## 📄 许可证 (License)

本项目基于 [MIT License](LICENSE) 开源。您可以自由地使用、修改和分发。

---
<div align="center">
Made with ❤️ by [您的名字/昵称]
</div>