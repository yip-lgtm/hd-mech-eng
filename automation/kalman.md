# Kalman Filter · 卡爾曼濾波

- Status: One of seven auto courses / 自學七科之一
- Exemption?: 控制進階 · 對照 MATLAB ode45／Simulink / 控制進階 · 對照 MATLAB ode45／Simulink
- Lab: https://yip-lgtm.github.io/hd-me-lab/#/auto/kalman
- Notes repo: https://github.com/yip-lgtm/hd-mech-eng/blob/main/automation/kalman.md

## Learning outcomes 學習成果

- Random: mean, variance, white noise
  - 隨機：均值、方差、白噪
- Predict: x⁻, P⁻ = F P Fᵀ + Q
  - 預測：x⁻、P⁻ = F P Fᵀ + Q
- Gain K, update x and P
  - 增益 K、更新 x、P
- Master 1-D first, then matrices
  - 一維先上手，再矩陣

## Notes 筆記

- Why not just average: Measurements are noisy, the model drifts; trust both a little
  - 點解唔好平均晒就算：量測嘈，模型會漂；兩邊都要信一啲
- Why not just average: Large K trusts z; small K trusts the prediction
  - 點解唔好平均晒就算：K 大：信新量測；K 細：信預測
- Why not just average: Large R (bad sensor) → small K
  - 點解唔好平均晒就算：R 大（感測差）→ K 細
- The predict–update two-step: Predict uses F, Q — no z yet
  - 預測–更新兩拍：預測用 F、Q，唔使 z
- The predict–update two-step: Update uses z, R, corrects x and P
  - 預測–更新兩拍：更新用 z、R，修正 x 同 P
- The predict–update two-step: P is uncertainty; after the filter it should beat the raw sensor
  - 預測–更新兩拍：P 係不確定度；濾波後應細過量測
- Join cybernetics and state space: Cybernetics: information; Kalman: optimal fusion
  - 同控制論、狀態空間接龍：控制論：資訊；卡爾曼：最優資訊融合
- Join cybernetics and state space: Engineering cybernetics: state; Kalman: state estimate
  - 同控制論、狀態空間接龍：工程控制論：狀態；卡爾曼：狀態估計
- Join cybernetics and state space: LQR + Kalman = LQG
  - 同控制論、狀態空間接龍：LQR + Kalman = LQG

## Workshop application 工作室

- Estimate state in noise. Predict (model) + update (measurement). Q trusts the model, R trusts the sensor. Standard in navigation and fusion.
  - 在噪聲入面估狀態。預測（模型）+ 更新（量測）。Q 信模型、R 信感測。機器人、導航、感測融合標準件。

## Formulas 公式

- x⁻ = F x    P⁻ = F P Fᵀ + Q — 預測
- K = P⁻ Hᵀ (H P⁻ Hᵀ + R)⁻¹ — 卡爾曼增益
- x = x⁻ + K(z − H x⁻) — 更新

