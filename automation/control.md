# Principles of Automatic Control · 自動控制原理

- Status: One of seven auto courses / 自學七科之一
- Exemption?: EME4208 儀錶與控制 · EME4273 自動化 / EME4208 儀錶與控制 · EME4273 自動化
- Lab: https://yip-lgtm.github.io/hd-me-lab/#/auto/control
- Notes repo: https://github.com/yip-lgtm/hd-mech-eng/blob/main/automation/control.md

## Learning outcomes 學習成果

- Block diagrams, G(s), open/closed loop
  - 方塊圖、傳函、開環／閉環
- Time domain: overshoot, ts, steady-state error
  - 時域：超調、ts、穩態誤差
- PID: Kp speed, Ki offset, Kd damping
  - PID：Kp 快、Ki 消差、Kd 阻尼
- Routh, Bode, Nyquist stability
  - Routh、Bode、Nyquist 穩定性

## Notes 筆記

- Open vs closed loop: Open loop is fast but hates model error and disturbance
  - 開環 vs 閉環：開環快但怕模型同干擾
- Open vs closed loop: Negative feedback cuts gain sensitivity
  - 開環 vs 閉環：負反饋減增益敏感度
- Open vs closed loop: Positive feedback grows error into oscillation
  - 開環 vs 閉環：正反饋會把誤差放大至振盪
- The three PID terms: P: effort ∝ error; ess is usually not zero
  - PID 三項：P：誤差大就出力大，ess 通常唔零
- The three PID terms: I: piles error, kills offset; too much windup
  - PID 三項：I：累積誤差，消死區，太多會積分飽和
- The three PID terms: D: predicts, cuts overshoot, hates noise
  - PID 三項：D：預估，抑超調，對噪聲敏感
- Stability entry: Poles in the LHP first
  - 穩定性入口：極點在左半平面先穩
- Stability entry: Bode: gain margin, phase margin
  - 穩定性入口：Bode：增益裕度、相位裕度
- Stability entry: Tune PID below; watch overshoot and ringing
  - 穩定性入口：調下面 PID，睇超調同振盪

## Workshop application 工作室

- Core of the HD control module. Open/closed loop, PID, stability, time and frequency domain. The Simulink mass–spring is a second-order plant.
  - HD 控制科主力。開／閉環、PID、穩定性、時域同頻域。Simulink 質量–彈簧就係二階對象。

## Formulas 公式

- u = Kp e + Ki ∫e dt + Kd ė — PID
- ess = lim s→0  s E(s) — 終值定理穩態誤差
- ζ, ωn   2ζωn, ωn² — 二階標準型

