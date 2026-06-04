# Evaluation of Radar Range Using Scilab
## Aim
To calculate the maximum range of a radar system using the Radar Range Equation and verify the results through Scilab programming.

## Theory
The Radar Range Equation is a key relationship used in radar system design to determine the maximum distance (range) at which a radar can detect a target.

It is expressed as:


## Algorithm

1.Initialize constants:
  λ (wavelength) = 0.03 m
  σ (radar cross section) = 1 m²

2.Vary each parameter while keeping the others constant:
  Pt: 0.1 → 10
  Gt: 1 → 50
  Pm: 1e⁻¹⁵ → 1e⁻¹⁰

3.Compute maximum range using: R_max = ((Pt * Gt² * λ² * σ) / ((4π)³ * Pm))¼

4.Plot the following:
  Pt vs Rmax
  Gt vs Rmax
  Pm vs Rmax
  
## Procedure

1.Refer to the Algorithm and write the Scilab code for the experiment.

2.Open Scilab on your system.

3.Create a New Editor File:
   Go to File → New → Script.

4.Type Your Code in the editor window.

5.Save the File with a suitable name (e.g., radar_range.sce).

6.Execute the Code:
    Press F5 or click Execute → File with echo.

## Code
```
clc;
clear;
close;
Pt = 1000;
Gt_dB = 30;
Gr_dB = 30;
Gt = 10^(Gt_dB/10);
Gr = 10^(Gr_dB/10);
f = 10e9;
c = 3e8;
lambda = c/f;
sigma = 1;
Pr_min = 1e-12;
R = 1000:1000:100000;
Pr = (Pt * Gt * Gr * lambda^2 * sigma) ./ ...
     (((4*%pi)^3) * (R.^4));
Pr_dB = 10 * log10(Pr);
Pt_req = (Pr_min * ((4*%pi)^3) .* (R.^4)) ./ ...
         (Gt * Gr * lambda^2 * sigma);
Pt_dB = 10 * log10(Pt_req);
scf(1);
plot(R/1000, Pr_dB, 'b');
xlabel('Range (km)');
ylabel('Received Power P_r (dB)');
title('Received Power vs Range');
xgrid();
scf(2);
plot(R/1000, Pt_dB, 'r');
xlabel('Range (km)');
ylabel('Required Transmitted Power P_t (dB)');
title('Transmitted Power vs Range');
xgrid();
disp("Frequency (GHz) = " + string(f/1e9));
disp("Wavelength (m) = " + string(lambda));
disp("Gt = " + string(Gt_dB) + " dB");
disp("Gr = " + string(Gr_dB) + " dB");

```
## Output
<img width="1918" height="1110" alt="image" src="https://github.com/user-attachments/assets/9d0c152a-8f1a-4226-9d25-2c7d593c64ae" />

<img width="1918" height="1116" alt="Screenshot 2026-06-04 174920" src="https://github.com/user-attachments/assets/25887153-fa04-4a2f-aec9-ffd93b992567" />

## Manual Calculation
<img width="1334" height="800" alt="WhatsApp Image 2026-06-04 at 5 52 28 PM" src="https://github.com/user-attachments/assets/e79ff5e5-6d47-486b-a761-9c11d23fc847" />

## Result
Thus, the maximum range of a radar system calculated using the Radar Range Equation is successfully verified using Scilab programming.
