# SolidWorks · SolidWorks

- Status: Lab page live / 自學分頁已開
- Exemption?: EME3212 → EME4279 3D CAD / EME3212 → EME4279 3D CAD
- Lab: https://yip-lgtm.github.io/hd-me-lab/#/solidworks
- Notes repo: https://github.com/yip-lgtm/hd-mech-eng/blob/main/cad/solidworks.md

## Learning outcomes 學習成果

- 草圖：直線、尺寸、幾何關係（中點、垂直、重合）
  - 草圖：直線、尺寸、幾何關係（中點、垂直、重合）
- Boss-Extrude / Cut-Extrude / Revolve
  - Boss-Extrude / Cut-Extrude / Revolve
- 圓角、倒角、孔向導
  - 圓角、倒角、孔向導
- 組合：重合、同心、距離配合
  - 組合：重合、同心、距離配合

## Notes 筆記

- 新零件同單位: File → New → Part
  - 新零件同單位：File → New → Part
- 新零件同單位: 右下角單位改 MMGS（圖係 mm 唔好用 IPS）
  - 新零件同單位：右下角單位改 MMGS（圖係 mm 唔好用 IPS）
- 新零件同單位: File Properties 填 drawing number、作者
  - 新零件同單位：File Properties 填 drawing number、作者
- Boss-Extrude 大件: Front Plane → Sketch
  - Boss-Extrude 大件：Front Plane → Sketch
- Boss-Extrude 大件: 畫封閉 80 × 50 長方形，標尺寸
  - Boss-Extrude 大件：畫封閉 80 × 50 長方形，標尺寸
- Boss-Extrude 大件: Features → Extruded Boss/Base，深度 15
  - Boss-Extrude 大件：Features → Extruded Boss/Base，深度 15
- Boss-Extrude 大件: Origin 對準圖上黑點
  - Boss-Extrude 大件：Origin 對準圖上黑點
- Extruded Cut 剪階梯: 揀要剪嘅面 → Sketch
  - Extruded Cut 剪階梯：揀要剪嘅面 → Sketch
- Extruded Cut 剪階梯: 由右上角畫 33 × 25 長方形蓋住要冇嘅料
  - Extruded Cut 剪階梯：由右上角畫 33 × 25 長方形蓋住要冇嘅料
- Extruded Cut 剪階梯: Features → Extruded Cut（唔好再 Boss）
  - Extruded Cut 剪階梯：Features → Extruded Cut（唔好再 Boss）
- Extruded Cut 剪階梯: End Condition：Through All 或 Blind = 件厚
  - Extruded Cut 剪階梯：End Condition：Through All 或 Blind = 件厚
- Extruded Cut 剪階梯: 預覽黃色箭嘴指住要剪走嘅料；反咗就 Reverse Direction
  - Extruded Cut 剪階梯：預覽黃色箭嘴指住要剪走嘅料；反咗就 Reverse Direction
- 常見錯誤: Cut 掣灰：未 Exit Sketch，或者 profile 未封閉
  - 常見錯誤：Cut 掣灰：未 Exit Sketch，或者 profile 未封閉
- 常見錯誤: 幾塊藍色區域：用 Selected Contours 只揀一個封閉形
  - 常見錯誤：幾塊藍色區域：用 Selected Contours 只揀一個封閉形
- 常見錯誤: 件消失：方向反或 Blind 大過件厚
  - 常見錯誤：件消失：方向反或 Blind 大過件厚
- 常見錯誤: 菱形／交叉線：Convert Entities 連中點會變 X，階梯 cut 唔使
  - 常見錯誤：菱形／交叉線：Convert Entities 連中點會變 X，階梯 cut 唔使

## Workshop application 工作室

- 中小企業、模具、夾具、HD 工場作業最常見。先 Boss-Extrude 大件，再用 Extruded Cut 剪階梯——唔好喺錯誤 sketch 上硬切。
  - 中小企業、模具、夾具、HD 工場作業最常見。先 Boss-Extrude 大件，再用 Extruded Cut 剪階梯——唔好喺錯誤 sketch 上硬切。

## Formulas 公式

- S — 快捷工具列
- Esc — 退出指令
- Ctrl+8 — 正視當前 sketch
- Space — 視圖定向
- MMGS — 毫米單位
- Cut-Extrude — 剪料

