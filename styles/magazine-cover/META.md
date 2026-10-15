# 杂志封面式

```yaml
id: magazine-cover
name: 杂志封面式
input_modes: [text, image]
subjects: [person]
outputs: [keyvisual, sheet]
default_ratio: "3:4"
required_fields: [角色参考图, 角色设定]
optional_fields: [文字层]
source: styles/magazine-cover/STYLE.md
style_anchors:
  - 杂志封面版式：顶部强个性刊名区 + 居中角色主体 + 四周封面线
  - 刊名区占画面高约 18%–25%、横向占宽 60% 以上
  - 角色可越过刊名区，头部遮挡部分刊名（封面惯例）
  - 封面线 1–3 条、小号无衬线，不遮脸与标志物
  - 期号 / 日期 / 条码位放边角，装饰总面积 ≤5%
keyvisual_shape_adaptation:
  - 三层版式：刊名区 / 主体区 / 信息区，层级清楚
  - 角色半身或全身居中，视线看向刊名区或直视读者
  - 封面线围绕主体、不侵入脸部
  - 刊名可被角色遮挡一部分，但主体仍可读
sheet_shape_adaptation:
  - 顶部保留刊名位、四周保留封面线位，中段做姿态分区
  - 沿用同一刊名区尺寸与封面线规则，多格只换姿态与视角
  - 分区之间用留白与光区分，不画网格线与边框
  - 刊名区保留；封面线改成视角 / 表情标签位
must_preserve:
  - 刊名区 + 主体区 + 信息区的三层版式
  - 封面线 1–3 条且不遮脸
  - 强个性刊名字与明显更小的封面线字
  - 边角的期号 / 日期 / 条码位
avoid_when_applying_to_keyvisual:
  - 真实杂志或报纸名、报头 nameplate、外文品牌水印
  - 只有一张普通插画、没有刊名区与封面线
  - 超过 3 条封面线或封面线遮脸
  - 多种强调色、霓虹发光
  - 反平庸：不得套通用杂志版式——刊名的字体个性、与角色的咬合方式（遮多少、怎么压）必须为这个角色定
avoid_when_applying_to_sheet:
  - 网格线、边框、角标
  - 各格刊名区尺寸或封面线规则不一致
  - 把不同姿态做成不同成像
```
