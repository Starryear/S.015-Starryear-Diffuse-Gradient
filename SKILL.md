---
name: starryear-diffuse-gradient
description: Transform a user photograph into a vertical 9:16 diptych with untouched 16:9 photographic evidence above a night-toned, gradient-first surreal reconstruction. Use for S.015、星年·弥散渐变、夜色柔光、上原图下生成图. Do not use for a simple filter, daytime pastel treatment, or a generated copy of the evidence panel.
---

# 【S.015】Starryear-Diffuse-Gradient丨星年·弥散渐变

Create one borderless, text-free 9:16 artwork. A real 16:9 photo crop spans the top; a larger source-derived diffuse-gradient reconstruction fills the bottom. Preserve the theme and identity anchors while changing composition, scale, space, or material.

## Workflow

1. Read the [Chinese production prompt](references/starryear-diffuse-gradient-prompt.zh-CN.md), or its [English equivalent](references/starryear-diffuse-gradient-prompt.en.md). Request a source photograph if none was supplied.
2. Inspect the source. Select a safe 16:9 crop, 1–3 identity anchors, 3–5 source colors, one main surreal mechanism, and at most one supporting mechanism.
3. Generate only the lower panel using the source as reference. Let 65–80% of its area read as smooth, low-detail, overlapping freeform color fields; recognizable anchors occupy 20–35%. Include one off-canvas field and one field dissolving an anchor. Preserve open colored shadows, sufficient midtones, and a single broad restrained glow.
4. Check the thumbnail for gradient-first hierarchy and recognizable theme. Inspect at 100% for noise, fibers, hard edges, banding, black voids, identity drift, and unrelated objects. If needed, revise the prompt and retry once.
5. Use [scripts/compose_9x16.py](scripts/compose_9x16.py) with Python and Pillow to combine the actual source and generated lower panel. Default output: 1152×2048; evidence: 1152×648; artwork: 1152×1400. Choose crop bias to protect the subject.
6. Verify exact dimensions and that the top contains only resized/cropped source pixels. Show the final image with one short sentence describing the crop anchor, surreal proposition, and color fields.

## Guardrails

- Never redraw, retouch, recolor, extend, erase, or generate the evidence panel. Only proportional resizing and cropping are allowed.
- The lower panel is a reconstruction, not a blurred or filtered repaint. Invention must derive from visible source elements.
- Keep 35–50% quiet colored dark space. Use non-black night tones, clean continuous gradients, translucent falloff, and selective clarity. No smoke texture, stars, nebulae, neon outlines, visible grain, paper, or hard glass UI.
- No text, watermark, frame, unrelated fantasy props, or accidental extra subjects.
- Examples are user-approved showcase works only. Never reuse their subjects, colors, or composition for a different source photograph.
