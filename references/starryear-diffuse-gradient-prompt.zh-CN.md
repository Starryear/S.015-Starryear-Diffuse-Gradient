# 【S.015】Starryear-Diffuse-Gradient丨星年·弥散渐变

把任意照片制作成一张完整的 9:16 竖版作品：最上方是真实原图的 16:9 裁切证据带，下方是同一主题的夜间弥散渐变超现实重构。上方证明“它来自哪里”，下方回答“它还能变成什么”。

## 不可变成品结构

- 最终画布固定为竖版 9:16，推荐 1152×2048 或等比例分辨率。
- 顶部证据带横跨全宽，固定为 16:9。1152 宽画布时高度为 648 px；余下 1400 px 全部属于生成区。
- 证据带必须位于最顶端；生成区紧接其下。默认无边框、无留白、无标题、无 Logo、无水印。
- 分界可以干净直接，也可让下方色光在接缝处产生轻微呼应，但生成内容不得覆盖证据带。

## 原图证据硬约束

- 客户照片只能做等比缩放和 16:9 裁切，不调色、不滤镜、不修图、不扩图、不补画、不删改内容。
- 选择裁切位置时优先保护脸、主体、手、标志物和关键关系；默认中心裁切不合适时，自适应上移、下移或左右偏移。
- 不把照片交给生成模型制作顶部区域。先生成下方艺术图，再用确定性图像合成把客户原文件嵌入顶部。
- 最终检查顶部像素内容确实来自客户原文件；AI 模拟得再像也不能替代真实证据。

## 先读懂照片

生成前明确：

1. 主题：照片真正讲的是什么，而不只是物体名称。
2. 识别骨架：最少哪些特征能维持人物身份、动物物种、建筑结构、风景空间或物体功能。
3. 原图的主方向、尺度关系、视线中心、明暗节奏和 3–5 个源色。
4. 哪些关系必须保留，哪些形体可以被放大、悬浮、重复、融化、穿透或转化。

## 下方不是照抄

- 保留主题、情绪和关键识别骨架，但重新设计构图、尺度、空间与材质；不得只是把原照片模糊、调色或重新画一遍。
- 从照片已有元素中选择一个核心母题，进行显著但可追溯的艺术转化。第一眼应感到不同，第二眼仍能认出与原图的关系。
- 默认选择一个主超现实命题，并最多增加一个辅助机制，避免效果堆砌：
  - 尺度失常：一个源元素成为巨大环境或微型世界。
  - 失重悬浮：主体、碎片或影子脱离重力形成新的节奏。
  - 物质转化：实体逐步变成光雾、半透明膜、液态渐变或空气色场。
  - 空间反转：内外、远近、上下、容器与被容纳物发生可信但不可能的互换。
  - 时间回声：同一源形体以不同透明度、尺度和景深出现，表达运动或记忆，而非简单复制。
  - 环境生成：主体的一部分生长为地形、天空、光带或空间结构。
- 禁止无依据地添加飞船、星球、传送门、眼睛、巨型人物或其他通用“超现实素材”。陌生感必须从当前照片生长出来。

## 先把“弥散渐变”做对

本 Skill 中的弥散渐变不是夜景、烟雾、景深虚化或给写实画面加 Bloom。它是 **gradient-first 的抽象色场构成**：少量大尺度自由渐变点或无定形色块相互覆盖，颜色在没有硬边的情况下连续渗混；物象只作为嵌入色场的识别锚点。第一眼必须先看见色块关系和明暗流向，第二眼才认出原图主题。

### 色场硬指标

- 生成区至少 65% 的视觉面积由平滑、低细节的连续色场主导；可识别物象与清晰纹理合计不超过约 35%。不得生成一张完整写实场景再叠雾。
- 使用 3–5 个不对称、尺度不同、彼此部分重叠的自由色场。至少一个色场从画外进入，至少一个跨越主体或与另一个色场混出清楚的第三种中间色；禁止均匀横向、纵向或同心径向渐变。
- 每个色场都要有明确的色核、极宽的半透明衰减区和完全消失的边缘。看见圆形光斑边界、椭圆贴片、喷枪圈、镜头光晕圈或硬色带即失败。
- 色场必须有尺度层级：一个主色场承担视线中心，1–2 个次色场形成方向和冷暖关系，其余仅作低亮支撑。不能把所有颜色做成同亮度、同大小的发光团。
- 使用深海蓝、墨紫、蓝灰、夜绿或原图暗色作非纯黑基底；从原图提取 3–5 个源色并向相邻夜光色偏移。高饱和颜色只能占小面积，白色只作柔和过渡或唯一主亮核。
- 画面保留 35–50% 的安静暗场或低密度渐变。暗场也要有轻微色相和明度漂移，不能成为纯黑空洞。
- 允许前层半透明膜、中层色雾、后层低亮环境光，但这些层仍应读作大色场，不应被渲染成云海、星云、烟尘、花瓣雨或具象天空。
- Bloom 只用于一个主色核，且必须宽、软、低对比；不能沿物体轮廓发光。加入近乎不可见的均匀抖动以防色带，不得出现粗颗粒、纸纹、水彩沉淀、粉笔或喷漆脏点。

### 洁净、亮度与朦胧感

- 保留原版柔和、流动、半透明、略带梦境感的弥散气质；“干净”只约束画面杂质，不得把色场改成硬边几何、玻璃 UI、产品渲染或机械式光学结构。
- 整体亮度比常规深夜画面提高约一档：暗部仍为有色深蓝、墨紫或夜绿，但不能大面积压成黑块；中间调必须充足，主亮核柔和通透，不得炸白。
- 朦胧来自极宽的色彩衰减、透明层叠和低对比过渡，不来自烟尘、颗粒、模糊滤镜或灰雾蒙版。
- 100% 查看时不得出现可感知噪点、粗颗粒、纤维、草丝状发光、毛发状线条、污点或压缩脏块；同时不得为了干净而抹平成塑料表面。
- 允许极低频、几乎不可察觉的柔和色流和空气感；禁止密集高频纹理、锐利折射线、规则硬边色带和过度锐化。

### 物象如何进入色场

- 只保留 1–3 个身份锚点。将其简化为裁切轮廓、半透明剪影、低细节结构、局部清晰切片或被色场吞没的残影；不要完整重绘所有细节。
- 至少一个锚点必须被大色场穿透、遮没或溶解 30–70%，以证明色场是空间主体而不是背景装饰。
- 可有一个小范围相对清晰的锚点承担识别，其余锚点必须软化或抽象。清晰区域不得遍布全画面。
- 不以真实光源解释色场，不生成“夜晚的原场景”。颜色可以违背局部照明逻辑，但要保持连续、柔和、无硬边的混色逻辑。

### 一眼淘汰的伪弥散

出现以下任一项，应直接重做下方生成区：写实夜景占主导；主体纹理处处清晰；云海、星空、星云或浓烟成为背景；只有一个彩色光斑；线性双色渐变；明显圆形径向光晕；霓虹描边；镜头散景；大面积白色发光；颜色只贴在主体周围而没有跨画面的色场关系；可见噪点、颗粒、纤维或脏灰；硬边玻璃 UI；几何产品渲染感；暗部大面积死黑。

## 题材适配

- 人物：保留身份、脸部比例和姿态；可让服装、影子、头发或环境发生尺度/物质转化。不要制造陌生面孔。
- 动物：保留物种轮廓、头部与典型姿态；可将毛发、羽翼、运动路径转为夜色光雾。
- 植物：保留枝叶、花心或生长方向；可将局部放大为半透明空间、漂浮膜或时间回声。
- 风景：保留地平线、山水走势和空间层级；可反转天空与地面、让道路或水面成为发光流场。
- 建筑与城市：保留透视、天际线和标志性体块；可把窗格、倒影或立面节奏重组为悬浮空间。
- 静物、产品、食物：保留外轮廓与关键功能结构；可让材质、阴影、液体或内部空间发生不可能转化。不得虚构品牌文字。
- 车辆与机械：保留型号识别结构和比例；用速度回声、环境光流或局部透明化重构，不能随意增加零件。
- 多主体：保留原始关系与数量逻辑；回声和抽象层不得被误认为新增真实主体。

## 生成提示词必须包含

提示词要写出照片实际内容和所选超现实命题，并包含以下语义：

- same theme and recognizable identity anchors, but a newly staged composition
- substantial source-derived surreal transformation, not a copy or filtered repaint
- gradient-first abstract composition; the large diffuse color fields dominate before the subject is recognized
- 65–80% smooth low-detail color field, only 20–35% simplified recognizable anchors; not a fully rendered scene
- deep non-black night base with three to five asymmetrical, differently scaled, overlapping freeform mesh-gradient fields
- at least one off-canvas field and one field crossing through and dissolving a subject anchor; visible intermediate colors where fields overlap
- colored cores, extremely broad transparent falloff, fully dissolved edges, layered atmospheric depth
- a brighter luminous night exposure with open colored shadows and generous midtones, while retaining soft haze and low-contrast depth
- clean but not hard: no visible grain, noise, dirt, fibers or hair-like luminous detail; preserve soft misty color transitions without smoke texture
- one restrained broad bloom only; quiet dark breathing space; soft digital/holographic materiality
- no text, no watermark, no border, no unrelated fantasy objects

明确避免：fully rendered realistic scene、literal copy of the source composition、simple blurred photo、uniform Gaussian blur、subject fully sharp everywhere、background scenery、cloudscape、smoke、stars、nebula、bokeh、lens flare、single radial glow、linear two-color gradient、pure black void、cyberpunk neon outline、laser lighting、over-saturation、hard polygons、hard-edged glass UI、product-render geometry、generic space imagery、watercolor、gouache、paper texture、visible grain、sensor noise、fibers、hair-like luminous lines、plastic 3D gloss、duplicated limbs or subjects。

## 工作流与质检

1. 观察照片，确定顶部 16:9 安全裁切和下方的主题、识别骨架、源色及超现实命题。
2. 仅生成下方艺术区域；不要让生成模型承担顶部原图。
3. 先以缩略图检查：第一眼是否读成 3–5 个大色场及其重叠关系，而不是读成一幅夜景；若先看见完整写实主体，即判失败。
4. 再检查弥散硬指标：色场是否主导至少约 65% 面积；是否有画外进入、跨越锚点、混合中间色、完全消融的边缘、一处主 Bloom 和足够暗场。
5. 检查主题不变，识别骨架仍成立，且不存在无关物体、身份漂移、主体误增或缺失。
6. 以 100% 尺寸检查：画面应明亮一档且保持朦胧；若出现噪点、颗粒、纤维、脏灰、暗部结块或硬边产品渲染感，必须重做。
7. 检查渐变连续、亮部不炸白；不能依赖后期强降噪，也不能用硬边和塑料质感换取“干净”。
8. 使用 [scripts/compose_9x16.py](../scripts/compose_9x16.py) 或等价的确定性工具，把客户原图裁成顶部 16:9，并与生成区合成为 9:16。
9. 最后再次确认顶部未被任何生成处理，输出尺寸精确为 9:16。

若失败，重写提示词时不要只说“更模糊”或“降噪”。应保留原来的自由弥散色场和柔和层叠，删除会诱发颗粒、纤维和脏雾的词，明确 `brighter open shadows`、`clean soft haze`、`no visible grain or fibers`、`no hard-edged glass UI`，并指定哪一个锚点被哪一个柔和色场穿透或溶解。若主题丢失，只恢复 1–3 个局部清晰锚点，不恢复完整原构图。最多主动重试一次，除非用户要求继续。

## 交付

展示最终 9:16 成品，并用一句话说明顶部裁切锚点、下方超现实命题和夜间弥散色场。默认不展示完整内部提示词。
