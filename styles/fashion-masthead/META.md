# 时尚大刊封面（fashion-masthead）

```yaml
id: fashion-masthead
name: 时尚大刊封面
input_modes: [text, image]
subjects: [person]
outputs: [keyvisual, sheet]
default_ratio: "3:4"
required_fields: [角色参考图, 角色设定]
optional_fields: [文字层]
source: styles/fashion-masthead/STYLE.md
style_anchors:
  - 满幅时装摄影打底，顶部超大高对比衬线刊名横贯
  - 刊名区占画面高 18%–25%、横向占宽 ≥75%
  - 主体可越过刊名区下缘，头部遮挡部分刊名（封面惯例）
  - 左右两侧各 1–2 条窄体无衬线封面线，不遮脸
  - 底部边角放期号 / 日期 / 条码位，装饰总面积 ≤5%
keyvisual_shape_adaptation:
  - 三层版式：刊名区 / 主体区 / 信息区，层级清楚
  - 主体满幅顶天立地，头部不等高、前后错落景深
  - 封面线围绕主体、不侵入脸部
  - 刊名可被主体遮挡一部分，但刊名主体仍可读
  - 多人组像时：前排至大腿、中排至腰、后排仅头肩，互相轻微遮挡
sheet_shape_adaptation:
  - 顶部保留刊名位、两侧保留封面线位，中段做姿态分区
  - 沿用同一刊名区尺寸与封面线规则，多格只换姿态与视角
  - 分区之间用留白与光区分，不画网格线与边框
  - 封面线改成角色名 / 视角标签位
must_preserve:
  - 刊名区 + 主体区 + 信息区的三层版式
  - 刊名区横向 ≥75%、高对比衬线、全大写
  - 封面线每侧 1–2 条且不遮脸
  - 强个性刊名字与明显更小的封面线字
  - 边角的期号 / 日期 / 条码位
avoid_when_applying_to_keyvisual:
  - 真实杂志或报纸名、报头 nameplate、外文品牌水印
  - 只有一张普通插画、没有刊名区与封面线
  - 每侧超过 2 条封面线或封面线遮脸
  - 多种强调色、霓虹发光、3D 立体字
  - 网格线 / 分格边框 / 编号标签
  - 反平庸：刊名的字体个性、与主体的咬合方式（遮多少、怎么压）必须为这组角色定
avoid_when_applying_to_sheet:
  - 网格线、边框、角标
  - 各格刊名区尺寸或封面线规则不一致
  - 把不同姿态做成不同成像
```
