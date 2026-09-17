<h1 align="center">【S.015】Starryear-Diffuse-Gradient丨星年·弥散渐变</h1>
<p align="center">让照片保留真实，让色彩在夜色里重新生长。</p>
<p align="center">
<img src="https://img.shields.io/badge/Codex-Skill-111111" alt="Codex Skill">
<a href="LICENSE.md"><img src="https://img.shields.io/badge/Usage-Non--Commercial-355C65" alt="Usage"></a>
<img src="https://img.shields.io/badge/Language-中文%20%2F%20English-586C7C" alt="Language">
</p>

## ⚠️ 声明

© 2026 Starryear年. All rights reserved.

本项目可用于个人学习、非营利研究及不产生商业收益的个人创作。商业产品、收费服务、客户委托、企业业务、付费教学、商业 AI Agent / Workflow、转售及商业分发，均须事先取得 Starryear年 的书面许可。发布非商业作品时，欢迎注明来源并 **@Starryear年**。完整条款见 [LICENSE.md](LICENSE.md)。

## 📖 关于本项目

**星年·弥散渐变**将一张照片转译为一幅竖版双联作品：顶部保留未经重绘的真实照片，下方让源于照片的色彩、轮廓与情绪进入柔和、半透明的夜色渐变场。主题依然可辨，构图、尺度、空间与材质可以重新展开。

- 固定 9:16 竖版，顶部为横跨全宽的 16:9 原图证据带。
- 下方以大尺度弥散色场为主，保留 1–3 个关键识别锚点。
- 配色从每张照片提取，适用于人物、植物、风景、建筑和静物等题材。
- 原图只允许等比缩放和裁切；下方独立生成后再确定性合成。

不用于普通模糊滤镜、写实夜景重绘、霓虹描边或无关幻想素材堆叠。

## 🖼️ 示例作品

以下两张成品由用户提供并指定用于本次发布，按原文件收录。示例仅展示效果，不作为其他照片的固定主体、配色或构图模板。

<table>
<tr><td width="50%"><img src="assets/examples/01-ritual-diffuse.jpg" alt="民俗仪式与红蓝夜色弥散" width="100%"></td><td width="50%"><img src="assets/examples/02-lotus-diffuse.png" alt="荷叶与青绿弥散色场" width="100%"></td></tr>
<tr><td align="center">民俗 · 色彩展开</td><td align="center">荷叶 · 透明流动</td></tr>
</table>

## 📋 目录

- [下载 Skill](#️-下载-skill)
- [使用方法](#-使用方法)
- [可自由调整的部分](#️-可自由调整的部分)
- [核心原则](#-核心原则)
- [内容结构](#-内容结构)
- [许可证](#-许可证)

## ⬇️ 下载 Skill

[下载「【S.015】Starryear-Diffuse-Gradient丨星年·弥散渐变」完整压缩包](S.015-Starryear-Diffuse-Gradient.zip?raw=true)

## 🚀 使用方法

### 方式一：作为 Codex Skill 使用

下载并解压 ZIP，将其中的 `starryear-diffuse-gradient` 文件夹放入个人 Skills 目录，随后在支持 Skill 的会话里上传照片并调用：

```text
使用 $starryear-diffuse-gradient 处理这张照片。
顶部保留真实原图，下方进行夜色弥散渐变重构。
```

### 方式二：作为提示词直接使用

| 语言 | 完整提示词 |
| --- | --- |
| 中文 | [中文生产提示词](references/starryear-diffuse-gradient-prompt.zh-CN.md) |
| English | [English production prompt](references/starryear-diffuse-gradient-prompt.en.md) |

将提示词与原照片交给支持参考图的图像生成工具，仅生成下方艺术区。顶部必须使用原文件合成，不能让模型模拟。合成脚本需要 Python 与 Pillow：

```bash
python scripts/compose_9x16.py source.jpg lower.png final.png --crop center
```

`--crop` 支持 `center`、`top`、`bottom`、`left`、`right`。默认输出 1152×2048；如需自定义尺寸，须同时保持整体 9:16 与顶部 16:9 的整数像素比例。

## 🎛️ 可自由调整的部分

| 参数 | 调整方向 |
| --- | --- |
| 裁切位置 | 优先保护主体、脸部、手部与关键关系 |
| 超现实命题 | 尺度失常、悬浮、物质转化、空间反转、时间回声或环境生成 |
| 源色关系 | 从当前照片提取 3–5 色，转为相邻夜光色 |
| 识别锚点 | 保留 1–3 处局部清晰特征，其余进入色场 |
| 输出分辨率 | 保持固定比例，按用途提高分辨率 |

## 💡 核心原则

1. **原图是真实证据。** 只缩放、只裁切，不重绘、不调色、不覆盖。
2. **色场先于物象。** 下方约 65–80% 为连续低细节色场，识别锚点约占 20–35%。
3. **陌生感来自原片。** 选择一个主超现实命题，最多一个辅助机制。
4. **夜色依然通透。** 保持有色暗部、充足中间调与一处克制柔光，避免死黑与炸白。
5. **朦胧来自渐变。** 不以烟尘、颗粒、纸纹或均匀模糊代替透明层叠。

## 📁 内容结构

```text
starryear-diffuse-gradient/
├── README.md
├── LICENSE.md
├── SKILL.md
├── agents/openai.yaml
├── references/
│   ├── starryear-diffuse-gradient-prompt.zh-CN.md
│   └── starryear-diffuse-gradient-prompt.en.md
├── scripts/compose_9x16.py
└── assets/examples/
    ├── 01-ritual-diffuse.jpg
    └── 02-lotus-diffuse.png
```

仓库根目录另提供完整 ZIP。`assets/examples/` 只收录本次明确指定的展示成品，执行 Skill 时不默认复用示例内容。

## 📄 许可证

详见 [LICENSE.md](LICENSE.md)。商业使用请联系 **Starryear年** 获取书面授权。

如果这个方法对你有帮助，欢迎点亮 Star，也欢迎分享并 @Starryear年，让我看到照片在你手中的另一种可能。
