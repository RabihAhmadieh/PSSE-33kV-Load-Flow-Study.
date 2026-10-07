# PSS/E Load Flow Study: 33 kV Network and Inverter Duty Transformer

**Author:** Rabih Al Ahmadieh  
**Study type:** First PSS/E training project - steady-state load flow  
**Status:** Documented simulation screenshot; transformer data verification pending.

![PSS/E load-flow single-line diagram](Images/PSSE_Load_Flow_SLD.png)

## Project objective
Model a 33 kV grid connection, a 10 km transmission line, and a five-winding inverter duty transformer supplying four low-voltage loads. Review the grid supply, voltage profile, and active-power balance.

This portfolio project documents my first PSS/E model, using a Power Projects training assignment. It demonstrates input preparation and interpretation of a load-flow diagram. It is an educational study.

## Network inputs

| Component | Supplied data |
|---|---|
| Grid | 33 kV, 50 Hz, 450 MVA three-phase short-circuit level, X/R = 10 |
| Line | 10 km; R = 0.136 ohm/km; X = 0.404 ohm/km; B = 2.84e-6 S/km |
| Transformer | 13.2 MVA; 33/0.69/0.69/0.69/0.69 kV; 130 kW load loss; 7% impedance |
| Vector group | Y d11 d11 d11 d11, as specified in the Word assignment |
| Loads | Two at 3.300 MW and two at 3.125 MW; total 12.850 MW |

The 10 km line length and vector group are stated in the supplied Word assignment. The workbook records the load quantities. No load power factor or reactive-power demand is explicitly provided in the supplied text; the screenshot shows approximately zero reactive demand at the loads.

## Results visible in the supplied screenshot

| Quantity | Approximate displayed value |
|---|---:|
| Grid active-power supply | 13.1 MW |
| Grid reactive-power supply | 0.6 MVAr |
| Grid bus voltage | 1.00 pu / 33.0 kV |
| Bus 101 voltage | 0.98 pu / 32.4 kV |
| LV bus voltages (201, 301, 401, 501) | 0.98 pu |
| Connected active load from input workbook | 12.850 MW |

The difference between the rounded grid supply and specified load is approximately 0.25 MW. This is an indicative total network loss only: precise losses require unrounded PSS/E output. The screenshot rounds the LV voltage to 0.7 kV and load flows to one decimal place; use the pu values and original inputs for interpretation.
