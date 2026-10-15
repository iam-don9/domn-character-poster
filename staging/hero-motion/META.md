# 高能动作

```yaml
id: hero-motion
name: 高能动作
input_modes: [text, image]
subjects: [person]
outputs: [keyvisual, sheet]
default_ratio: "3:4"
required_fields: [角色参考图, 角色设定]
optional_fields: [能力类型]
source: staging/hero-motion/STAGE.md
staging_anchors:
  - 角色处在运动的顶点，读得出明确的动势方向
  - 重心偏移、躯干扭转、四肢不对称开合
  - 衣摆 / 披风 / 发梢被风与惯性带起，形成动势线
  - 手正在做一件事：触发 / 释放 / 握武器 / 推 / 伸 / 比手势
  - 低角度仰拍为主，透视强度按动作方向给
pose_vocabulary:
  - 悬空
  - 跃起
  - 街跳
  - 蹲起
  - 浮现
  - 冲刺
sequence_logic:
  - 起势：重心下沉蓄力
  - 爆发：蹬地离地，动势线最强
  - 滞空：四肢舒展的顶点帧
  - 签名定格：最可截图的一帧
camera_angles:
  - 低角度仰拍（跃起 / 冲刺首选）
  - 平视（横向冲刺，动势线横穿画面）
  - 轻微俯拍（下落 / 落地瞬间）
must_preserve:
  - 动势方向单一明确
  - 重心偏移、非站定
  - 手部动作明确
  - 衣摆发梢的惯性拖尾
avoid:
  - 静态站姿摆拍
  - 无重心的漂浮
  - 泛词：帅气 / 炫酷 / 强烈的动感 / 速度感极强
  - 左右对拉的对抗式构图
  - 四肢全对称的跳伞式姿势
pairs_well_with: [hud-keyart, cinematic-onesheet]
conflicts_with: [minimal-editorial]
```
