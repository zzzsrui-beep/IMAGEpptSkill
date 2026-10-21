# IMAGEpptSkill

一套从主题到演示文稿的 PPT 技能，包含生成图片型幻灯片、将图片转换为可编辑 PPTX，以及串联两步的一键流程。

## 三个技能

- **IMAGEskill**：根据主题或内容生成每页幻灯片图片，并合成为图片型 PPTX。
- **PPTskill**：将幻灯片图片或截图还原为可编辑 PPTX；文字为文本框，视觉元素以图片层呈现。
- **SUPERskill**：先生成幻灯片图片，再转换为可编辑 PPTX，同时保留中间素材。

## 使用

在 Codex 中按需指定技能，例如：

- `使用 IMAGEskill，围绕人工智能医疗做一份 8 页图片版 PPT。`
- `使用 PPTskill，把 ./slides/slide1.png 转成可编辑 PPTX。`
- `使用 SUPERskill，围绕新能源车市场做一份 10 页并可编辑的 PPT。`

SUPERskill 会依赖同目录中的 IMAGEskill 和 PPTskill。生成幻灯片图片需要 Codex 的 imagegen 图像生成能力。

## 依赖

Python 3，以及 `python-pptx`、`Pillow`、`numpy`：

```bash
pip install python-pptx pillow numpy
```

需要转换为可编辑 PPTX 时，建议先准备清晰的幻灯片图片；输出文件和中间素材会写入任务目录。
