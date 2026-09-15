# MATLAB + Simulink · MATLAB + Simulink

- Status: Lab page live / 自學分頁已開
- Exemption?: EME3211 / 4212 / 4208 / 4213 / EME3211 / 4212 / 4208 / 4213
- Lab: https://yip-lgtm.github.io/hd-me-lab/#/matlab
- Notes repo: https://github.com/yip-lgtm/hd-mech-eng/blob/main/cad/matlab.md

## Learning outcomes 學習成果

- 矩陣運算、索引、腳本 vs 函數
  - 矩陣運算、索引、腳本 vs 函數
- plot / subplot / 標籤
  - plot / subplot / 標籤
- ode45 解 ẋ = f(t,x)
  - ode45 解 ẋ = f(t,x)
- Simulink：Gain、Integrator、Scope
  - Simulink：Gain、Integrator、Scope

## Notes 筆記

- 工作區同矩陣: A = [1 2; 3 4];  b = [5; 6];
  - 工作區同矩陣：A = [1 2; 3 4];  b = [5; 6];
- 工作區同矩陣: x = A \ b   % 解 Ax=b，唔好 inv(A)*b 做習慣
  - 工作區同矩陣：x = A \ b   % 解 Ax=b，唔好 inv(A)*b 做習慣
- 工作區同矩陣: whos、clear、clc 分清楚
  - 工作區同矩陣：whos、clear、clc 分清楚
- 繪圖: t = linspace(0, 2*pi, 400); plot(t, sin(t))
  - 繪圖：t = linspace(0, 2*pi, 400); plot(t, sin(t))
- 繪圖: xlabel ylabel title grid on legend
  - 繪圖：xlabel ylabel title grid on legend
- 繪圖: hold on 疊第二條曲線
  - 繪圖：hold on 疊第二條曲線
- ode45: 把二階 ODE 拆成一階系統：x1=x, x2=v
  - ode45：把二階 ODE 拆成一階系統：x1=x, x2=v
- ode45: f = @(t,y) [y(2); -w^2*y(1) - 2*z*w*y(2)]
  - ode45：f = @(t,y) [y(2); -w^2*y(1) - 2*z*w*y(2)]
- ode45: [t,y] = ode45(f, [0 10], [1; 0]); plot(t,y(:,1))
  - ode45：[t,y] = ode45(f, [0 10], [1; 0]); plot(t,y(:,1))
- Simulink 第一個模型: simulink → Blank Model
  - Simulink 第一個模型：simulink → Blank Model
- Simulink 第一個模型: 兩個 Integrator：ẍ→v、v→x
  - Simulink 第一個模型：兩個 Integrator：ẍ→v、v→x
- Simulink 第一個模型: Gain(-k/m)、Gain(-c/m) 回授到 Sum
  - Simulink 第一個模型：Gain(-k/m)、Gain(-c/m) 回授到 Sum
- Simulink 第一個模型: Scope 睇位移；對照 ode45 曲線應重叠
  - Simulink 第一個模型：Scope 睇位移；對照 ode45 曲線應重叠

## Workshop application 工作室

- 矩陣、繪圖、微分方程、系統模擬。HD 數學 II 同控制科用得到。Simulink 用方塊圖砌質量–彈簧–阻尼，唔使先寫晒程式。
  - 矩陣、繪圖、微分方程、系統模擬。HD 數學 II 同控制科用得到。Simulink 用方塊圖砌質量–彈簧–阻尼，唔使先寫晒程式。

## Formulas 公式

- help plot — 函式說明
- lookfor ode — 關鍵字搜尋
- doc ode45 — 瀏覽器文件
- simulink — 開庫
- ode45 — 數值積分
- A\b — 解線性方程

