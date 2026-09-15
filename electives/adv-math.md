# Advanced Engineering Mathematics · 高級工程數學

- Code: AEM
- Credits: 14
- Status: All open for study; award counts 2 / 自學全開；畢業只計 2
- Exemption?: 選修 · 接 EME4212 · MATLAB 主力 / 選修 · 接 EME4212 · MATLAB 主力
- Lab: https://yip-lgtm.github.io/hd-me-lab/#/electives/adv-math
- Notes repo: https://github.com/yip-lgtm/hd-mech-eng/blob/main/electives/adv-math.md

## Learning outcomes 學習成果

- Laplace tables, partial fractions, ODEs
  - 拉普拉斯表、部分分式、ODE
- Fourier series and transform
  - 傅立葉級數同變換
- Separation of variables: wave, heat entry
  - 分離變量：波動、熱方程入口
- Numerics: Newton, RK4, ode45
  - 數值：Newton、RK4、ode45

## Notes 筆記

- Laplace for ODEs: ICs into the formula, algebra for Y(s), invert
  - 拉普拉斯解 ODE：初值入公式，代數解 Y(s)，再反變換
- Laplace for ODEs: Complex poles → damped sinusoid = 2nd-order system
  - 拉普拉斯解 ODE：複極點 → 衰減正弦，就係二階系統
- Laplace for ODEs: Match EME4212 and control G(s)
  - 拉普拉斯解 ODE：對照 EME4212 同自控傳函
- Fourier for spectra: Periodic signals split into sines; a square wave needs many odd harmonics
  - 傅立葉睇頻譜：週期訊號拆正弦；方波要好多奇次諧波
- Fourier for spectra: Aperiodic → transform; sampling meets Nyquist from signals
  - 傅立葉睇頻譜：非週期用變換；取樣對照訊號科奈奎斯特
- Fourier for spectra: Vibration and acoustics: fundamental before waveform
  - 傅立葉睇頻譜：振動同聲學：主頻先於波形
- Numerics and MATLAB: Newton for f(x)=0: guess, tangent, repeat
  - 數值同 MATLAB：Newton 解 f(x)=0：猜、切線、重複
- Numerics and MATLAB: RK4 / ode45 for ẋ=f(t,x)
  - 數值同 MATLAB：RK4／ode45 解 ẋ=f(t,x)
- Numerics and MATLAB: Do not hand-expand an 18th-order determinant; use A\b
  - 數值同 MATLAB：唔好用手算十八階行列式；用 A\b

## Workshop application 工作室

- Laplace, Fourier, PDEs, numerics. Control, vibration and heat transfer all use this. Feeds automatic control and Kalman.
  - 拉普拉斯、傅立葉、PDE、數值方法。控制、振動、熱傳都用呢套。讀完可以直接餵自控同卡爾曼。

## Formulas 公式

- L{y'} = s Y − y(0) — 導數定理
- f(t) ~ a0/2 + Σ (an cos nωt + bn sin nωt) — 傅立葉級數
- ut = k uxx — 一維熱方程

