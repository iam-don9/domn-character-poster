# 时尚摆拍

```yaml
id: fashion-pose
name: 时尚摆拍
input_modes: [text, image]
subjects: [person]
outputs: [keyvisual, sheet]
default_ratio: "3:4"
required_fields: [角色参考图, 角色设定]
optional_fields: [能力类型, 张力档]
source: staging/fashion-pose/STAGE.md
staging_anchors:
  - 角色为镜头而摆，身体线条有设计感，像时装大片的一页
  - 张力可高可低：低端是雕塑式静态，高端是跃动失衡
  - 四肢讲究线条的延伸方向，不随意摆放
  - 手是造型的一部分：扶腰 / 撩发 / 拉衣领 / 插袋 / 甩袖 / 撑地
  - 表情不夸张；低端克制、高端有方向感与攻击性
tension_range:
  - 低 · 雕塑式：三角造型、重心单腿、脊背 S 形、肩线一高一低
  - 高 · 跃动式：离地或半离地、反向扭身、织物大幅飞扬、四肢极限拉伸、重心失衡
pose_vocabulary:
  - 走位
  - 回眸
  - 坐姿
  - 靠墙
  - 特写
  - 跃起
  - 甩袖转身
  - 撑地低伏
  - 逆风站定
  - 半空回眸
sequence_logic:
  - 低张力端：走位 → 回眸 → 坐姿 → 面部特写（杂志内页式）
  - 高张力端：蓄势 → 跃起 → 滞空顶点 → 落地回眸
camera_angles:
  - 低张力端：平视或略低，无透视畸变
  - 高张力端：低角度仰拍或斜角，允许适度透视夸张
must_preserve:
  - 线条有设计感，四肢有明确延伸方向
  - 手是造型的一部分
  - 表情不夸张
  - 高张力端必须有物理理由（风 / 雨 / 扬尘 / 起跳）
avoid:
  - 生活化的随意感
  - 影棚白底证件照式站姿
  - 默认选静的那一端（先问张力档）
  - 夸张表情、张嘴大笑
  - 泛词：高级 / 气质 / 气场
pairs_well_with: [magazine-cover, minimal-editorial, cinematic-onesheet, hud-keyart]
```
