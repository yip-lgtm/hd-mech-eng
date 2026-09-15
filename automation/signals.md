# Signals and Systems · 訊號與系統

- Status: One of seven auto courses / 自學七科之一
- Exemption?: EME4208 儀錶與控制 · 數學 II / EME4208 儀錶與控制 · 數學 II
- Lab: https://yip-lgtm.github.io/hd-me-lab/#/auto/signals
- Notes repo: https://github.com/yip-lgtm/hd-mech-eng/blob/main/automation/signals.md

## Learning outcomes 學習成果

- Continuous/discrete, periodic, energy/power
  - 連續／離散、週期、能量／功率
- LTI: superposition + time-invariance
  - LTI：疊加 + 時不變
- Impulse response h(t), y = h * u
  - 脈衝響應 h(t)，y = h * u
- Fourier spectrum, Laplace G(s)
  - 傅立葉頻譜、拉普拉斯 G(s)

## Notes 筆記

- Families of signals: A sinusoid is fixed by A, f, φ
  - 訊號家族：正弦由 A、f、φ 三個數決定
- Families of signals: Impulse δ(t) has area 1; sampling uses a δ-comb
  - 訊號家族：脈衝 δ(t) 面積 1，取樣用 δ 梳
- Families of signals: Step 1(t) is the prototype input of an integrator
  - 訊號家族：階躍 1(t) 係積分器嘅輸入原型
- LTI and convolution: Linear: a u1 + b u2 → a y1 + b y2
  - LTI 同卷積：線性：a u1 + b u2 → a y1 + b y2
- LTI and convolution: Time-invariant: u(t−t0) → y(t−t0)
  - LTI 同卷積：時不變：u(t−t0) → y(t−t0)
- LTI and convolution: h(t) determines the output for every input
  - LTI 同卷積：知道 h(t) 就知道所有輸入嘅輸出
- Sampling and Laplace: fs must exceed twice the highest frequency or you alias
  - 取樣同拉普拉斯：fs 要大於最高頻率兩倍，否則混疊
- Sampling and Laplace: s = σ+jω; RHP poles explode
  - 取樣同拉普拉斯：s = σ+jω，右半平面極點會爆發
- Sampling and Laplace: The RC G(s) is the system function from this course
  - 取樣同拉普拉斯：電路 RC 嘅 G(s) 就係訊號科嘅系統函數

## Workshop application 工作室

- Treat time functions as system inputs/outputs. LTI, convolution, Fourier and Laplace are the language of control and Kalman.
  - 把時間函數當成系統輸入／輸出。LTI、卷積、傅立葉、拉普拉斯係自控同卡爾曼嘅語言。

## Formulas 公式

- y(t) = ∫ h(τ) u(t−τ) dτ — 卷積
- X(s) = ∫ x(t) e^{−st} dt — 拉普拉斯
- ωs > 2 ω_max — 奈奎斯特取樣

