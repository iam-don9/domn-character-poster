# 电影一页海报式

```yaml
id: cinematic-onesheet
name: 电影一页海报式
input_modes: [text, image]
subjects: [person]
outputs: [keyvisual, sheet]
default_ratio: "3:4"
required_fields: [角色参考图, 角色设定]
optional_fields: [文字层]
source: styles/cinematic-onesheet/STYLE.md
style_anchors:
  - 经典 one-sheet 电影海报的排印传统：标题块 + 主视觉 + 底部 billing block 三段式
  - 主标题全大写、字距收紧，压在暗部或留白
  - 深色基调（深青 / 深褐 / 近黑）配最多一种强调色
  - 信息层级分明：主标题 > 角色 > 密集小字 billing block
  - 允许背景渐变营造电影感，但不发光
keyvisual_shape_adaptation:
  - 纵向三段：标题块 / 角色主视觉 / billing block，三段齐全
  - 标题块与 billing block 各占画面高约 12%–18%，主视觉占中段
  - 角色主视觉居中或按三分线偏置，环境背景托底
  - 标题可叠在角色下缘，但不遮脸与标志物
sheet_shape_adaptation:
  - 沿用同一深色基调与强调色，多格之间只换姿态与视角
  - 顶部保留标题位、底部保留小字位，中段做姿态分区
  - 分区之间用暗角与留白区分，不画网格线与边框
  - 三段式改成「标题块 + 多视角分区 + billing block 当标注位」
must_preserve:
  - 三段式版式与清晰的信息层级
  - 全大写收紧字距的主标题
  - 深色基调 + 最多一种强调色
  - 底部密集小字的 billing block
avoid_when_applying_to_keyvisual:
  - 杂志封面线、期号、条码位
  - 扁平插画缩略图感、商业模板感
  - 多种强调色
  - 霓虹、赛博蓝光、发光金属
  - 反平庸：三段式不得做成可替换的通用模板——标题块的位置 / 字符 / 与角色的咬合方式必须为这个角色定
avoid_when_applying_to_sheet:
  - 网格线、边框、角标
  - 各格强调色或基调不一致
  - 把不同姿态做成不同成像
```
