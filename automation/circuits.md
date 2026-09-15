# Electric Circuits · 電路

- Status: One of seven auto courses / 自學七科之一
- Exemption?: EME3228 / EME3229 / EME4206 / EME3228 / EME3229 / EME4206
- Lab: https://yip-lgtm.github.io/hd-me-lab/#/auto/circuits
- Notes repo: https://github.com/yip-lgtm/hd-mech-eng/blob/main/automation/circuits.md

## Learning outcomes 學習成果

- Ohm, series/parallel, dividers
  - 歐姆、串並聯、分壓分流
- KCL currents, KVL voltages
  - KCL 電流、KVL 電壓
- RC/RL first-order, time constant τ
  - RC／RL 一階，時間常數 τ
- Impedance, phasors, AC power
  - 阻抗、相量、交流功率

## Notes 筆記

- Ohm, series, parallel: Mark polarity and current before writing equations
  - 歐姆同串並聯：先標極性同電流方向再寫方程
- Ohm, series, parallel: Series: same I, add V. Parallel: same V, add I
  - 歐姆同串並聯：串聯電流同、電壓加；並聯電壓同、電流加
- Ohm, series, parallel: Divider: V1 = Vs · R1/(R1+R2)
  - 歐姆同串並聯：分壓：V1 = Vs · R1/(R1+R2)
- KCL/KVL by hand: Independent nodes = n−1, write KCL
  - KCL／KVL 手算：獨立節點數 = n−1，寫 KCL
- KCL/KVL by hand: Independent loops: KVL, drop = iR
  - KCL／KVL 手算：獨立迴路寫 KVL，電阻壓降 = iR
- KCL/KVL by hand: Do not claim EME3228 from ENGR 2405 grade D
  - KCL／KVL 手算：HD 唔好靠 ENGR 2405 D 去豁電科
- RC first-order and G(s): Capacitor: i = C dv/dt
  - RC 一階同傳函：電容：i = C dv/dt
- RC first-order and G(s): G(s)= Vc/Vs = 1/(τs+1), τ=RC
  - RC 一階同傳函：G(s)= Vc/Vs = 1/(τs+1)，τ=RC
- RC first-order and G(s): Settles near 5τ. Scope below: sweep R, C
  - RC 一階同傳函：5τ 近似到達終值。下面示波器可調 R、C

## Workshop application 工作室

- Ohm’s law, KCL/KVL and first-order RC circuits are the physics under transfer functions, control and Kalman. HD electrical modules start here.
  - 歐姆定律、KCL／KVL、RC 一階電路係之後傳函、控制同卡爾曼嘅物理底。HD 電科由呢度起。

## Formulas 公式

- V = I R — 歐姆定律
- Σ I_in = Σ I_out — KCL 節點電流
- Σ V_loop = 0 — KVL 迴路電壓
- τ = R C    y(t)=1−e^{−t/τ} — RC 單位階躍

