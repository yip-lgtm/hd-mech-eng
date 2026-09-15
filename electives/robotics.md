# Applied Robotics · 應用機械人學

- Code: ROBO
- Credits: 14
- Status: All open for study; award counts 2 / 自學全開；畢業只計 2
- Exemption?: 選修 · 接自動化／微機 / 選修 · 接自動化／微機
- Lab: https://yip-lgtm.github.io/hd-me-lab/#/electives/robotics
- Notes repo: https://github.com/yip-lgtm/hd-mech-eng/blob/main/electives/robotics.md

## Learning outcomes 學習成果

- Articulated / Cartesian / SCARA / Delta
  - 關節型／直角／SCARA／Delta
- DH: a, α, d, θ
  - DH：a, α, d, θ
- Forward T, inverse multiple solutions
  - 正運動學 T、逆解多解
- Teach pendant, I/O, light curtain
  - 教導盒、IO、安全光幕

## Notes 筆記

- Architectures: 6-axis articulated: dexterous, watch singularities
  - 構型：6 軸關節型：靈活、奇異點要避開
- Architectures: SCARA: fast horizontal, stiff vertical; Delta: light pick-and-place
  - 構型：SCARA：水平快、垂直剛；Delta：輕快拾放
- Architectures: Pick the architecture before the brand
  - 構型：選構型先於選牌子
- DH and solutions: Four numbers per link; the product is tool pose
  - DH 同解：每一桿四個數，連乘得出工具座標
- DH and solutions: Inverse may have many sets; shops teach points more than closed form
  - DH 同解：逆解可能多組；工場用教導點多過純公式
- DH and solutions: Singularity: Jacobian rank drops, speeds explode
  - DH 同解：奇異：Jacobian 跌秩，速度爆
- Safety and I/O: Curtain, fence, reduced mode; stop if a person enters the cell
  - 安全同 IO：光幕、圍欄、縮減模式；人入工作區要停
- Safety and I/O: Gripper pneumatic or electric; vacuum cups need leak detect
  - 安全同 IO：夾爪氣壓或電動，真空杯有洩漏檢測
- Safety and I/O: PLC handshake: ready, done, fault
  - 安全同 IO：PLC 握手：準備、完成、故障

## Workshop application 工作室

- Open chains, DH parameters, forward/inverse kinematics, grippers and safety. Shop-floor arms join the automation module.
  - 開鏈機構、DH 參數、正／逆運動學、夾爪同安全。工場機械臂同自動化科接龍。

## Formulas 公式

- T = A1 A2 … An — 正運動學
- ẋ = J(q) q̇ — Jacobian
- τ = Jᵀ F — 靜力映射

