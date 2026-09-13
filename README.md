# Supporting data — LEO constellation placement for ground observation over Kazakhstan

Numerical data behind the figures and tables of the manuscript *Methodology and Performance Analysis of the LEO Satellite Constellation Placement for the Ground Observation Mission over Kazakhstan*.

| File | Content | Used in |
|---|---|---|
| `candidate_pool.json` | Seven-day re-evaluation of the candidate pool: `front` = final search archive, `cloud` = sampled one-day evaluations, `star` = selected 3×8 / 800 km / 56° design. Fields: `P` planes, `N` satellites per plane, `h` altitude (km), `inc` inclination (deg), `Tmean_h` area-weighted mean revisit (h), `t100_h` time to full coverage (h), `cov24` first-24-h coverage fraction, `worst_h` / `p95_h` worst-point and area-weighted 95th-percentile maximum gap (h). | Fig. 2 |
| `inclination_scan.csv` | Framework simulation of the 3×8 Walker constellation at 800 km for inclinations from 50° to 98.6° (1310-point 0.5° grid, cos-latitude weights, seven days). Times in hours. | Table 1 |
| `plane_satellite_count_scan.csv` | Framework scan of plane count `P` (1–4) × satellites per plane `N` (1–12) at 800 km / 56°. Times in hours. | Fig. 3; 2×12 / 3×8 / 4×6 layout comparison |
| `grid_point_locations.csv` | STK coverage grid over Kazakhstan (815 points, nominal 0.5° Lat/Lon setting) with the cell areas used as weights. | Fig. 6(c); weights for all STK statistics |
| `coverage_timeseries_{56,85,98p6}deg.csv` | STK instantaneous and accumulated coverage (%) every 30 s, 10–17 Oct 2024. | Fig. 6(a), 6(b); t90 / t99 / t100 |
| `revisit_average_{56,85,98p6}deg.csv` | STK per-point average revisit time (s) at the 815 grid points. | Fig. 6(c), 6(d); area-weighted means 30.2 / 56.6 / 54.5 min |
| `revisit_maximum_{56,85,98p6}deg.csv` | STK per-point maximum revisit gap (s) at the 815 grid points, end gaps included. | Fig. 6(d); worst-point gaps 6.39 / 4.14 / 5.00 h |

STK settings: version 12.2, J2Perturbation propagator, Walker Delta 24/3/1, nadir-pointing sensors with 30° half-cone angle; `56`, `85` and `98p6` denote the orbital inclination in degrees.
