# 日杂动作

```yaml
id: daily-editorial
name: 日杂动作
input_modes: [text, image]
subjects: [person]
outputs: [keyvisual, sheet]
default_ratio: "3:4"
required_fields: [角色参考图, 角色设定]
optional_fields: [能力类型]
source: staging/daily-editorial/STAGE.md
staging_anchors:
  - 角色在做一件日常小事，姿态松弛、像被随手拍下的一帧
  - 重心落在一条腿上，肩膀不平齐，四肢不做三角造型
  - 手正在用：拿杯子 / 翻书页 / 拨头发 / 插兜 / 整理衣角 / 撑下巴
  - 不看镜头，或极轻的不经意的笑
  - 平视或略高，中景为主，单一自然光源方向
pose_vocabulary:
  - 靠墙 / 靠桌 / 靠窗框
  - 身体略前倾或侧靠
  - 低头看手里的东西
  - 侧身回头
sequence_logic:
  - 生活四格切片：四件不同的小事或四个日常场景
  - 同一个人、同一套光，四格之间只换动作与场景
  - 光的方向与色温保持一致
camera_angles:
  - 平视
  - 略高（显柔和）
  - 中景为主，不追求全身完整
must_preserve:
  - 非摆拍感，读得出"正在做某件事"
  - 自然的不对称（肩不齐、重心单腿）
  - 不看镜头
  - 单一自然光源方向
avoid:
  - 影棚摆拍感、硬凹姿势、三角造型
  - 直视镜头的模特脸
  - 超现实光效、强对比戏剧光
  - 泛词：自然 / 随性 / 高级感
pairs_well_with: [minimal-editorial, magazine-cover]
conflicts_with: [hud-keyart]
```
