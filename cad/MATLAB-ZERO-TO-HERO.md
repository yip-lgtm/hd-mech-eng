# MATLAB + Simulink · Zero to Hero

Target: EG524701 PTE · evening 4–6 h/week · 8 weeks then keep-alive.
Maps to: EME3211 Math I · EME3226 Principles · EME3228 Electricity · EME4208 Control · EME4212 Math II · EME4213 Dynamics.
Lab page: https://yip-lgtm.github.io/hd-me-lab/#/matlab
Scratch notes stay in `cad/matlab.md`.

## Access

1. MathWorks account: https://www.mathworks.com/mwaccount/
2. MATLAB Online (browser, no install): https://matlab.mathworks.com/
3. Desktop if IVE / student licence is on the machine: open MATLAB, type `ver`
4. Free Onramps work in browser even without a full toolbox licence:
   - MATLAB Onramp — https://matlabacademy.mathworks.com/details/matlab-onramp/gettingstarted
   - Simulink Onramp — https://matlabacademy.mathworks.com/details/simulink-onramp/simulink
   - Circuit Simulation Onramp — after electricity starts
   - Control Design Onramp with Simulink — before EME4208

Rule: every session ends with **one saved figure or one .slx** in a folder `matlab-lab/weekN/`. Do not only watch.

---

## Week 0 · 90 min · machine + first plot

**Done when:** you can open MATLAB, run a script, save a PNG.

```matlab
%% week0_sine.m
clc; clear; close all
t = linspace(0, 2*pi, 400);
y = sin(t);
plot(t, y, 'LineWidth', 1.4)
xlabel('t (rad)'); ylabel('sin t'); title('week 0')
grid on
print(gcf, 'week0_sine.png', '-dpng', '-r150')
```

Habits:
- `clc` clears command window. `clear` wipes workspace. `close all` closes figures.
- `whos` lists variables. Never `inv(A)*b` as a habit — use `A\b`.
- `help plot` · `doc ode45` · `lookfor integrat`

---

## Week 1 · MATLAB Onramp + arrays · 4 h

Official course first (about 2 h). Then drill:

```matlab
A = [1 2; 3 4];
b = [5; 6];
x = A \ b          % Ax = b
A(1,:)             % row 1
A(:,2)             % col 2
A'                 % transpose
linspace(0,10,21)
0:0.5:10
```

**Done when:** Onramp certificate saved as PDF + you can index a matrix without guessing.

Studio: put 3 load cases into a 3×2 matrix `[F, L]` and compute moments `M = F.*L`.

---

## Week 2 · scripts vs functions + plots · 4 h

Script = a tape you press play. Function = reusable tool with inputs/outputs.

```matlab
function [sigma, tau] = beam_stress(M, V, I, Q, t)
% M bending, V shear, I second moment, Q first moment, t thickness
sigma = M ./ I;          % simplify later with actual y
tau   = V .* Q ./ (I .* t);
end
```

Plot checklist every time: `xlabel ylabel title grid on legend`. Use `subplot` for 2 views.

```matlab
t = linspace(0, 4*pi, 600);
subplot(2,1,1); plot(t, sin(t)); grid on; title('x')
subplot(2,1,2); plot(t, cos(t)); grid on; title('v')
```

**Done when:** one `.m` function you can call from another script.

---

## Week 3 · linear algebra for ME · 4 h

This is EME3211 / 4212 muscle.

- Solve statics: `K \ F` for spring networks / truss-style 2–3 DOF
- Residual check: `norm(A*x - b)` should be ~1e-12, not 0.3
- Eigenvalues later: `eig(A)` for modes — peek only

Mini project — 2-spring in series / parallel:

```matlab
k1 = 200; k2 = 350; F = 80;   % N/m, N
K_series = 1/(1/k1 + 1/k2);
delta = F / K_series;
```

**Done when:** you trust `\` more than `inv`.

---

## Week 4 · ode45 · mass–spring–damper · 5 h

Second-order ODE must become first-order. State: $x_1=x,\ x_2=v$.

$$
\ddot x + 2\zeta\omega\dot x + \omega^2 x = f(t)/m
$$

```matlab
m = 2; c = 1.2; k = 80;
w = sqrt(k/m); z = c/(2*sqrt(k*m));
f = @(t,y) [y(2); -(k/m)*y(1) - (c/m)*y(2)];
[t,y] = ode45(f, [0 8], [0.04; 0]);   % 40 mm step, 0 velocity
plot(t, y(:,1)*1000); xlabel('t (s)'); ylabel('x (mm)'); grid on
```

Change `c` three times (under / critical / over). Save one figure with `legend`.

**Done when:** you can explain why two Integrators appear in Simulink next week.

Studio: clamp / hoist bounce — pick m, k from a real shelf load.

---

## Week 5 · Simulink Onramp + first plant · 5 h

1. Finish Simulink Onramp (~2 h).
2. Blank model. Same MSD as Week 4:
   - `Sum` → `Gain(1/m)` → Integrator (`v`) → Integrator (`x`)
   - Feedback: `Gain(-k)` from x, `Gain(-c)` from v, into Sum
   - `Scope` on x
   - Solver: ode45, stop time 8 s
3. Overlay Scope vs Week 4 `plot`. Curves must sit on top of each other.

Blocks you actually need this year: Gain, Sum, Integrator, Scope, Step, Sine Wave, Mux, To Workspace, Saturation.

**Done when:** screenshot of Scope + MATLAB plot look the same.

---

## Week 6 · MATLAB ↔ Simulink · 4 h

- `From Workspace` / `To Workspace` (`timeseries` or structure with time)
- `sim('msd')` from a script; sweep `k` in a `for` loop
- Subsystem: box the plant, name in/out `F`, `x`, `v`

```matlab
for k = [40 80 160]
    % set_param or use a masked parameter; start by editing Gain by hand
end
```

**Done when:** one script runs the model three times and plots three x(t).

---

## Week 7 · control (EME4208 trailer) · 5 h

Open loop vs P vs PI on the same plant.

1. Reference `Step` of 0.02 m
2. Error = ref − x
3. `Gain(Kp)` → plant force
4. Add Integrator on error for PI
5. Watch overshoot and steady-state error

Optional free course: Control Design Onramp with Simulink.

Do **not** start Adaptive / LQR / Kalman until this PI plot is clean.

**Done when:** one figure — open loop, P, PI on the same axes.

---

## Week 8 · electricity + report habit · 5 h

You will sit EME3228 (do not claim ENGR 2405 D). Use MATLAB here, not exemption.

- Series RL step: same ode45 pattern, state = current
- KVL loop as `A\b` for a 2-mesh DC circuit
- Circuit Simulation Onramp if you want Simscape Electrical later

Report habit (use in every HD lab):

```matlab
set(gcf, 'Color', 'w')
set(gca, 'FontSize', 11)
legend('Location','best')
print(gcf, 'fig_msd_pi.png', '-dpng', '-r200')
```

**Hero checkpoint:** you can (1) write a function, (2) integrate an ODE, (3) match it in Simulink, (4) close a PI loop, (5) export a labelled figure. That is enough for Y1–Y2. Everything else is DLC.

---

## After week 8 · pick by module, not by FOMO

| When the module is near | Add this only |
|---|---|
| EME4213 Dynamics | 2-DOF, `ode45` state length 4, mode shapes `eig` |
| EME4202 Fluids | 1-D pipe / tank ODE, not CFD |
| EME4224 Thermo | lumped RC thermal, same as MSD |
| EME4273 Automation | Stateflow Onramp, then a 2-state machine |
| EME4211 Design | parameter sweep + `fminbnd` on a cost |

Skip until needed: Deep Learning, RoadRunner, Vehicle Dynamics Blockset, code generation, Kalman notes in `automation/`.

---

## Daily 20-min drill (if a week slips)

1. Type one matrix and solve `A\b`.
2. Plot two curves with labels.
3. Change one number in last week's model and say what should happen *before* you press Run.

## Common traps

- Mixing degrees and radians in `sin` — MATLAB is radians.
- Algebraic loop in Simulink: you wired output straight back with no Integrator / delay.
- `inv(A)` on a near-singular stiffness matrix.
- Scope looks “right” but sample time is discrete 0.1 s on a 10 Hz plant — set solver to auto / ode45 first.
- Saving only the `.slx` and losing the parameters that lived in the workspace.

## Command crib

| Want | Type |
|---|---|
| Docs | `doc ode45` |
| Onramp Simulink | `learning.simulink.launchOnramp("simulink")` |
| Start library | `simulink` |
| Solve Ax=b | `x = A \ b` |
| Integrate | `[t,y] = ode45(f,tspan,y0)` |
| Run model | `simOut = sim("msd")` |
