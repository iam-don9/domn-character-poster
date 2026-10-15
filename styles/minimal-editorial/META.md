# 极简编辑式

```yaml
id: minimal-editorial
name: 极简编辑式
input_modes: [text, image]
subjects: [person]
outputs: [keyvisual, sheet]
default_ratio: "3:4"
required_fields: [角色参考图, 角色设定]
optional_fields: [文字层, 背景方案]
source: styles/minimal-editorial/STYLE.md
style_anchors:
  - 克制的研究出版物式编辑版式，纯色背景 + 大面积留白
  - 一个衬线主标题作为第一视觉与结构中心
  - 角色是唯一视觉中心，占画面高约 55%–70%，四周留呼吸空间
  - 2–4 个无功能平衡色块，总面积不超过 5%
  - 固定纯色背景方案（陶土橙 / 深黑 / 暖灰 / 鼠尾草绿 / 雾霾蓝），不渐变
keyvisual_shape_adaptation:
  - 主标题 + 角色主体 + 留白共同构成唯一视觉中心
  - 只显示一个主标题；有称号时最多加一行且字级更低
  - 装饰元素可接近或回应标题，但不遮挡标题、不遮脸
  - 不加栏目标签、页码、日期、网址或无意义说明
sheet_shape_adaptation:
  - 沿用同一纯色背景与单一强调色，多格只换姿态与视角
  - 主标题位固定在留白区，中段做姿态分区
  - 分区之间用留白区分，不画网格线与边框
  - 上限：1 主位 + 2 视角；超过即失去大留白特性，须换原子
must_preserve:
  - 一个主标题、一个视觉中心
  - 一个固定纯色背景方案，不渐变
  - 衬线主标题 + 克制无衬线辅字
  - 大面积留白与 2–4 个 ≤5% 的平衡色块
avoid_when_applying_to_keyvisual:
  - 复制任何机构的 Logo、字标、品牌署名或官方版式
  - 商业广告、发布会视觉、PPT 封面感
  - 复杂信息图、大量文字、3D、渐变、霓虹、发光
  - 多种强调色、均匀装饰阵列、UI 按钮状元素
  - 反平庸：极简最容易滑向"安全的好看"——留白必须有理由（为标题与主体让位），色块不得随机摆放
avoid_when_applying_to_sheet:
  - 网格线、边框、角标
  - 各格背景方案或强调色不一致
  - 把不同姿态做成不同成像
```
