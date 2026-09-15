# Microcomputer Principles · 微機原理

- Status: One of seven auto courses / 自學七科之一
- Exemption?: EME4208 儀錶 · EME4273 自動化 / EME4208 儀錶 · EME4273 自動化
- Lab: https://yip-lgtm.github.io/hd-me-lab/#/auto/mcu
- Notes repo: https://github.com/yip-lgtm/hd-mech-eng/blob/main/automation/mcu.md

## Learning outcomes 學習成果

- CPU, bus, ROM/RAM/I/O map
  - CPU、匯流排、ROM／RAM／I/O 映像
- Binary, two’s complement, bit ops
  - 二進制、補碼、位元運算
- GPIO, timers, PWM
  - GPIO、定時器、PWM
- ADC quantisation, interrupt vs poll
  - ADC 量化、中斷 vs 輪詢

## Notes 筆記

- von Neumann and the map: Instructions and data share a bus (von Neumann)
  - 馮·諾依曼同映像：指令同數據走同一匯流排（von Neumann）
- von Neumann and the map: ROM holds code, RAM variables, I/O takes addresses
  - 馮·諾依曼同映像：ROM 放程式，RAM 放變數，I/O 佔地址
- von Neumann and the map: Read a sensor = read an address; write a motor = write one
  - 馮·諾依曼同映像：讀感測器 = 讀某個地址；寫馬達 = 寫某個地址
- ADC/DAC and quantisation: More bits → finer staircase → smaller quantisation error
  - ADC／DAC 同量化：位元愈多，樓梯愈密，量化誤差愈細
- ADC/DAC and quantisation: Anti-alias filter before you sample
  - ADC／DAC 同量化：先抗混疊濾波再取樣
- ADC/DAC and quantisation: DAC or PWM can drive a motor’s average voltage
  - ADC／DAC 同量化：DAC + PWM 可驅動電機平均電壓
- Interrupts and real time: Polling wastes cycles; interrupts sleep until the event
  - 中斷同即時：輪詢浪費週期；中斷先瞓、事件先醒
- Interrupts and real time: Control loops often use a timer interrupt at fixed Ts
  - 中斷同即時：控制迴路常用定時器中斷固定 Ts
- Interrupts and real time: Keep ISRs short: read ADC, write PWM, set a flag
  - 中斷同即時：ISR 要短：讀 ADC、寫 PWM、設旗標

## Workshop application 工作室

- Controllers finally run on an MCU or PLC. Bits, memory, GPIO, ADC/DAC and interrupts connect sensors to motors.
  - 控制器最後跑喺微機／MCU／PLC。要識位、記憶體、GPIO、ADC／DAC、中斷，先接到感測同馬達。

## Formulas 公式

- q = (Vref−Vmin) / (2^n − 1) — n 位 ADC 量化步
- D = round((V−Vmin)/q) — 數碼碼
- duty = t_on / T    Vavg = duty · Vcc — PWM 平均電壓

