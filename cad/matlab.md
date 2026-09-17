# MATLAB + Simulink · MATLAB + Simulink

- Status: S0–S2 live / 2026-09-16 自學進行中（未裝桌面版）
- Exemption?: EME3211 / 4212 / 4208 / 4213 — 工具不是豁免
- Lab: https://yip-lgtm.github.io/hd-me-lab/#/matlab
- Path: [MATLAB-ZERO-TO-HERO.md](MATLAB-ZERO-TO-HERO.md)
- Notes repo: https://github.com/yip-lgtm/hd-mech-eng/blob/main/cad/matlab.md

## Learning outcomes 學習成果

- 開戶 + Onramp（瀏覽器，唔使裝）
- linspace / plot / 單位 mm→m
- 矩陣運算、索引、腳本 vs 函數
- ode45 解 ẋ = f(t,x)
- Simulink：Gain、Integrator、Scope

## Now 今堂（S2）

```matlab
%% s02_sine.m
clc; clear; close all
t = linspace(0, 4*pi, 500);
plot(t, sin(t), 'LineWidth', 1.4); hold on
plot(t, cos(t), 'LineWidth', 1.4)
xlabel('t (rad)'); ylabel('value'); title('s02: x and v')
legend('sin t','cos t'); grid on
```

```matlab
%% s02_spring.m
k = 800;                 % N/m
x_mm = [0 2 4 6 8];
x = x_mm / 1000;         % m
F = k * x;               % N
plot(x_mm, F, '-o', 'LineWidth', 1.4)
xlabel('deflection (mm)'); ylabel('F (N)'); grid on
disp(F(end))             % must be 6.4
```

## Notes 筆記

- 工作區：clc 清窗；clear 清變數；close all 關圖；whos 睇表
- 矩陣：A = [1 2; 3 4]; b = [5; 6]; x = A \ b
- 唔好 inv(A)*b 做習慣
- 繪圖：linspace + xlabel ylabel title grid on legend
- sin / cos 用弧度
- F=kx 先轉米：8 mm = 0.008 m，k=800 → 6.4 N
- ode45：二階拆一階 x1=x, x2=v
- Simulink：兩個 Integrator ¨x→v→x；Gain(-k) · Gain(-c) 回 Sum

## Workshop application 工作室

- S2：層架 / 夾具估 k，F=kx 表
- 之後：ode45 + Simulink 質量–彈簧–阻尼同一條物理

## Formulas 公式

- help plot — 函式說明
- linspace — 平均切點
- doc ode45 — 瀏覽器文件
- simulink — 開庫
- A\b — 解線性方程

## Personal notes 個人筆記

y=mx+c
