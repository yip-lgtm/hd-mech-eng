# Automation · 自動化系統

- Code: EME4273
- Credits: 14
- Status: All open for study; award counts 2 / 自學全開；畢業只計 2
- Exemption?: 選修 · 手冊 Sem 8 範例 1 · 14 cr / 選修 · 手冊 Sem 8 範例 1 · 14 cr
- Lab: https://yip-lgtm.github.io/hd-me-lab/#/electives/automation
- Notes repo: https://github.com/yip-lgtm/hd-mech-eng/blob/main/electives/automation.md

## Learning outcomes 學習成果

- Pneumatic symbols, cylinders, valves, sequence
  - 氣壓符號、缸、閥、順序圖
- PLC ladder: contacts, coils, timers
  - PLC 梯級：觸點、線圈、計時器
- Sensors: prox, photo, encoder
  - 感測：接近、光電、編碼器
- Safety circuit, e-stop, interlock
  - 安全迴路、急停、互鎖

## Notes 筆記

- Pneumatic circuits: Single/double acting; 5/2 valve reverses
  - 氣壓回路：單作用／雙作用缸，5/2 閥做換向
- Pneumatic circuits: Throttle for speed; do not use a regulator as a speed valve
  - 氣壓回路：節流閥調速，唔好靠減壓當調速
- Pneumatic circuits: Sequence A+ B+ A− B−: draw the displacement–step chart first
  - 氣壓回路：順序：A+ B+ A− B−，先畫位移–步序圖
- PLC ladder: Contacts left, coils right; scan top to bottom
  - PLC 梯級：左觸點、右線圈；掃描週期由上到下
- PLC ladder: Seal-in: start in parallel with the running coil
  - PLC 梯級：自我保持：起動並聯已運行之線圈
- PLC ladder: TON delay, CTU count, compare for position
  - PLC 梯級：TON 延時、CTU 計數、比較塊做位置
- Safety and sensing: E-stop is hard-wired; do not rely on code alone
  - 安全同感測：急停硬線切斷，唔好只靠程式
- Safety and sensing: Interlock: two cylinders must not extend together
  - 安全同感測：互鎖：兩缸唔好同時伸
- Safety and sensing: After this module, take the seven-course auto path for circuits and PID
  - 安全同感測：讀完呢科，去自動化七科補電路同 PID

## Workshop application 工作室

- PLC, pneumatics, sensors, sequential control. Shop-floor version of HD instrumentation. Full seven-course automation path (circuits → Kalman) is linked below.
  - PLC、氣壓、感測、順序控制。HD 儀錶科嘅工場版。下面有完整自動化七科自學（電路→卡爾曼）。

## Formulas 公式

- F = p A — 氣缸推力
- T_on = n · T_scan — PLC 計時器約數
- v = ω r — 編碼器線速度

