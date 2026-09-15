# Cybernetics · 控制論

- Status: One of seven auto courses / 自學七科之一
- Exemption?: 概念層 · 對照 EME4208 閉環 / 概念層 · 對照 EME4208 閉環
- Lab: https://yip-lgtm.github.io/hd-me-lab/#/auto/cybernetics
- Notes repo: https://github.com/yip-lgtm/hd-mech-eng/blob/main/automation/cybernetics.md

## Learning outcomes 學習成果

- Feedback: sense → compare → act → sense
  - 反饋：測 → 比 → 動 → 再測
- Information, noise, channel
  - 資訊同噪聲、通道
- Steady state, oscillation, purpose
  - 穩態、振盪、目的
- Man–machine, organisation, automata
  - 人機系統、組織、自動機

## Notes 筆記

- Feedback before formulae: Open loop: command out, no look at the result
  - 反饋先於公式：開環：指令直出，唔睇結果
- Feedback before formulae: Closed loop: output corrects input — purpose appears
  - 反饋先於公式：閉環：用輸出修正輸入，先有「目的」
- Feedback before formulae: Thermostat, pupil, governor share this structure
  - 反饋先於公式：恆溫、瞳孔、調速器都係同一結構
- Information and noise: Sensing is always noisy; cybernetics treats it as information
  - 資訊同噪聲：感測永遠有噪；控制論當資訊問題
- Information and noise: Channel capacity limits how small an error you can hold
  - 資訊同噪聲：通道容量限制你能控幾細嘅誤差
- Information and noise: Kalman is this line engineered
  - 資訊同噪聲：卡爾曼就係呢條線嘅工程化
- Boundary with control theory: Cybernetics: structure, information, adaptation, man–machine
  - 同自控原理分界：控制論：結構、資訊、適應、人機
- Boundary with control theory: Control theory: models, stability, PID, frequency domain
  - 同自控原理分界：自控原理：模型、穩定性、PID、頻域
- Boundary with control theory: Engineering cybernetics: Qian Xuesen wrote it as engineering
  - 同自控原理分界：工程控制論：錢學森把控制論寫成工程學

## Workshop application 工作室

- Wiener’s Cybernetics (1948): control and communication in the animal and the machine. Feedback, information, purposeful behaviour — not the same as a classical control textbook.
  - Wiener《Cybernetics》(1948)：動物同機器入面嘅控制同通訊。核心係反饋、資訊、目的性行為。唔等於自動控制原理教科書。

## Formulas 公式

- e = r − y — 誤差 = 參考 − 輸出（負反饋）
- H(s) = G/(1+G K) — 單位負反饋閉環

