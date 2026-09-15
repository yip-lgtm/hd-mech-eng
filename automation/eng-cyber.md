# Engineering Cybernetics · 工程控制論

- Status: One of seven auto courses / 自學七科之一
- Exemption?: EME4213 動力學 · 控制進階 / EME4213 動力學 · 控制進階
- Lab: https://yip-lgtm.github.io/hd-me-lab/#/auto/eng-cyber
- Notes repo: https://github.com/yip-lgtm/hd-mech-eng/blob/main/automation/eng-cyber.md

## Learning outcomes 學習成果

- State x, ẋ = A x + B u
  - 狀態 x，ẋ = A x + B u
- Output y = C x + D u
  - 輸出 y = C x + D u
- Controllability rank[B AB …], observability
  - 能控性 rank[B AB …]、能觀性
- State feedback u = −K x, a glance at LQR
  - 狀態反饋 u = −K x，LQR 一瞥

## Notes 筆記

- State is more than position: State = the smallest set that predicts the future
  - 狀態唔只係位置：狀態 = 預知未來所需嘅最少變量
- State is more than position: Mass–spring: x1 = position, x2 = velocity
  - 狀態唔只係位置：質量–彈簧：x1=位移，x2=速度
- State is more than position: Split a high-order ODE into first-order vectors, ss()
  - 狀態唔只係位置：高階 ODE 拆成一階向量，MATLAB ss()
- Controllable / observable: Controllable: some u steers any x in finite time
  - 能控／能觀：能控：用 u 可喺有限時間去到任意 x
- Controllable / observable: Observable: x can be rebuilt from the history of y
  - 能控／能觀：能觀：由 y 嘅歷史可重建 x
- Controllable / observable: Kalman observability = you may estimate the state
  - 能控／能觀：卡爾曼能觀 = 可以估狀態
- State feedback: u = −K x places poles when controllable
  - 狀態反饋：u = −K x 可搬極點（能控時）
- State feedback: Unmeasured states: observer or Kalman
  - 狀態反饋：量唔到嘅狀態用觀測器／卡爾曼
- State feedback: LQR picks K from J=∫(xᵀQx + uᵀRu)
  - 狀態反饋：LQR 用 J=∫(xᵀQx + uᵀRu) 揀 K

## Workshop application 工作室

- Qian Xuesen, Engineering Cybernetics (1954): cybernetic method for engineering systems. Today: state space, controllability/observability, optimal control.
  - 錢學森 1954《工程控制論》：用控制論方法處理工程系統。而家課程對應狀態空間、能控能觀、最優控制。

## Formulas 公式

- ẋ = A x + B u — 狀態方程
- y = C x + D u — 輸出方程
- Wc = [B AB A²B …] — 能控性矩陣

