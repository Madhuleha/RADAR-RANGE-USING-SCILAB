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

```
## Output


## Manual Calculation

## Result
Thus, the maximum range of a radar system calculated using the Radar Range Equation is successfully verified using Scilab programming.
