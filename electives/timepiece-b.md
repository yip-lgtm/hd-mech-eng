# Timepiece Technology Studies B · 時計科技研修 B

- Code: TPSB
- Credits: 14
- Status: All open for study; award counts 2 / 自學全開；畢業只計 2
- Exemption?: 選修 · 石英、測試、組裝 / 選修 · 石英、測試、組裝
- Lab: https://yip-lgtm.github.io/hd-me-lab/#/electives/timepiece-b
- Notes repo: https://github.com/yip-lgtm/hd-mech-eng/blob/main/electives/timepiece-b.md

## Learning outcomes 學習成果

- Quartz 32768 Hz and division
  - 石英振盪 32768 Hz 分頻
- CMOS circuit, stepper coil
  - CMOS 電路、步進摩打線圈
- Battery, leakage, hack
  - 電池、漏電流、停秒
- Test: rate, water resist, functions
  - 測試：日差、防水、功能

## Notes 筆記

- Quartz and division: Crystal sets the frequency; temperature compensation sets rate
  - 石英同分頻：晶體穩頻，溫度補償決定日差
- Quartz and division: 15 binary stages: 32768 → 1 Hz
  - 石英同分頻：15 級二分頻：32768 → 1 Hz
- Quartz and division: Same idea as MCU clocks and prescalers
  - 石英同分頻：對照微機科嘅時鐘同分頻器
- Stepper and battery: Coil pulse kicks the rotor; gears take it to the hands
  - 步進同電池：線圈脈衝推轉子，齒輪再去指針
- Stepper and battery: Short pulses save energy; leakage kills the cell
  - 步進同電池：脈衝要短，省電；漏電會瞓電池
- Stepper and battery: Discharge the cap when changing the cell, or the movement can lock
  - 步進同電池：換電池先放電電容器，防機芯鎖死
- Testing: Rate, amplitude (mech) or pulse width (quartz)
  - 測試：日差、振幅（機械）或脈衝寬（石英）
- Testing: Water test: air or vacuum; a stamp is not a diving licence
  - 測試：防水：氣壓或真空法，唔好當潛水證明亂戴
- Testing: Functions: date change, hack, lume
  - 測試：功能：日曆換日、停秒、夜光

## Workshop application 工作室

- Quartz movement, circuit, stepper, test and quality. A is mechanical, B is electromechanical. Take both.
  - 石英機芯、電路、步進摩打、測試同品質。A 科機械，B 科機電。兩科一齊先完整。

## Formulas 公式

- 32768 = 2^15 Hz — 二分頻 15 次到 1 Hz
- τ = I / (n · Φ) — 步進力矩概念
- rate = (T_meas − T_ref) / T_ref — 日差

