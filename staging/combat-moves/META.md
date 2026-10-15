# 战斗招式

```yaml
id: combat-moves
name: 战斗招式
input_modes: [text, image]
subjects: [person]
outputs: [keyvisual, sheet]
default_ratio: "3:4"
required_fields: [角色参考图, 角色设定]
optional_fields: [能力类型, 兵器载体]
source: staging/combat-moves/STAGE.md
staging_anchors:
  - 角色正在出手或刚收招，是打斗中的签名帧
  - 拧腰转胯、重心下压或前倾，发力链方向一致
  - 招式类型先定：投射 / 追踪 / 范围 / 近身 / 突袭 / 蓄力大招
  - 视线锁定对手或招式指向，表情冷峻不夸张
  - 低角度仰拍 / 斜角 / 极近特写
pose_vocabulary:
  - 起手
  - 命中
  - 收招
  - 定格
sequence_logic:
  - 起手：蓄力姿态，重心下压
  - 连击：出手瞬间，动势最强
  - 收招：惯性带身形缓转落定
  - 签名定格：最可截图的一帧
  - 招式类型可作位格标签（全英）
camera_angles:
  - 低角度仰拍（对峙 / 蓄力）
  - 斜角（命中瞬间的失衡感）
  - 极近特写（兵器碰撞点 / 拳锋）
must_preserve:
  - 发力链方向一致（脚 → 腰 → 肩 → 手）
  - 招式结合当前角色现造，不套成品招
  - 动势残影（衣摆 / 武器尾迹 / 发丝）
  - 冷峻克制的表情
avoid:
  - 泛词：打 / 攻击 / 挥舞 / 移动 / 冲过去 / 强烈 / 震撼 / 迅猛 / 炸裂 / 压迫感 / 帅气 / 华丽 / 酷炫
  - 静态站定
  - 空放特效（特效无发力源）
  - 回合节奏 / 慢拍 / 时间码（那是视频逻辑）
pairs_well_with: [hud-keyart, cinematic-onesheet]
conflicts_with: [minimal-editorial]
```
