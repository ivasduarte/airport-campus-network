# RCOMP 2025-2026: Project 1 Sprint 1 Member 1221176 File
=====

# Terminal 5

## 1. Scale and Measurements

* **Building Dimensions:** $400m × 150m = 60 000m²$
* **Scale Used:** $2.8cm <=> 50m -> 1cm ⇔ 17.86m$

---

## 2. Network Outlets Calculation

**Standard Rule:** Two outlets per 10m² of work area (`outlets = Work Area * 2`)
* **NOTE:** `Work Area = room area / 10`

---

## 2.1. Level 0 (Arrivals)

> Rooms **WITH** Standard Outlets: 3, 4, 5, 6, 7, 8, 9, 10, 11, 14, 15, 19, 20, and 21.

> Rooms **WITHOUT** Outlets: 1, 2, 12, 13, 16, 17, 18, and 22.

---

### Room Areas and Outlets Calculation

| ROOMS  | DIMENSIONS ($cm$) | DIMENSIONS ($m$) | AREA ($m^2$) |         WORK AREA          |  OUTLETS   |
|:------:|:-----------------:|:----------------:|:------------:|:--------------------------:|:----------:|
| **1**  |     0.7 x 0.7     |   12.5 x 12.5    |      -       |             -              |     -      |
| **2**  |     0.7 x 0.7     |   12.5 x 12.5    |      -       |             -              |     -      |
| **3**  |     2.2 x 0.8     |   39.3 x 14.3    |    561.99    | 561.99/10 = 56.199 ≈ 56 WA | 56*2 = 112 |
| **4**  |     1.3 x 0.8     |   22.2 x 14.3    |    371.46    | 371.46/10 = 37.146 ≈ 37 WA | 37*2 = 74  |
| **5**  |    1.25 x 0.8     |   22.3 x 14.3    |    318.89    | 318.89/10 = 31.889 ≈ 32 WA | 32*2 = 64  |
| **6**  |    1.95 x 0.8     |   34.8 x 14.3    |    497.64    | 497.64/10 = 49.764 ≈ 50 WA | 50*2 = 100 |
| **7**  |     1.1 x 0.8     |   19.6 x 14.3    |    280.28    | 280.28/10 = 28.028 ≈ 28 WA | 28*2 = 56  |
| **8**  |    1.95 x 0.8     |   34.8 x 14.3    |    497.64    | 497.64/10 = 49.764 ≈ 50 WA | 50*2 = 100 |
| **9**  |     1.3 x 0.8     |   22.2 x 14.3    |    317.46    | 317.46/10 = 31.746 ≈ 32 WA | 32*2 = 64  |
| **10** |    0.8 x 1.71     |   14.3 x 30.5    |    436.15    | 436.15/10 = 43.615 ≈ 44 WA | 44*2 = 88  |
| **11** |    0.7 x 1.71     |   12.5 x 30.5    |    381.25    | 381.25/10 = 38.125 ≈ 38 WA | 38*2 = 76  |
| **14** |     0.8 x 1.6     |   14.3 x 28.6    |    408.98    | 408.98/10 = 40.898 ≈ 41 WA | 41*2 = 82  |
| **15** |     1.4 x 0.9     |   25.0 x 16.1    |    402.50    | 402.50/10 = 40.250 ≈ 40 WA | 40*2 = 80  |
| **19** |     1.9 x 0.8     |   33.9 x 14.3    |    484.77    | 484.77/10 = 48.477 ≈ 49 WA | 49*2 = 98  |
| **20** |    2.25 x 0.8     |   40.2 x 14.3    |    574.86    | 574.86/10 = 57.486 ≈ 58 WA | 58*2 = 116 |
| **21** |     1.6 x 0.8     |   28.6 x 14.3    |    408.98    | 408.98/10 = 40.898 ≈ 41 WA | 41*2 = 82  |


**Total Standard Outlets for Level 0: 1192**

#### Schematic Plan (For Standard Outlets Only)
> This schematic shows an example layout for the outlets on the Level. The plan **is not** drawn to scale, as doing so
would make the diagram too difficult to read.

> When placing the outlets, no point in each room can be more than 3 meters away from one.

![Network Outlets Deployment Schematic Plan Level 0](doc/sprint1/1241176/assets/Terminal5_Level0-StandardOutlets.svg)

**(For clarity, outlets associated with Access Points will be shown on a separate schematic)**

---

## 2.2. Level 2 (Departures)

> Rooms **WITH** Standard Outlets: 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 23, 24, and 25.

> Rooms **WITHOUT** Outlets: 1, 2, 18, 19, 20, 21, 22, and 26.

> Rooms For **Hardware**: 1, 2, 22, and 26.


### Room Areas and Outlets Calculation

| ROOMS  | DIMENSIONS ($cm$) | DIMENSIONS ($m$) | AREA ($m^2$) |      WORK AREA       | OUTLETS | 
|:------:|:-----------------:|:----------------:|:------------:|:--------------------:|:-------:|
| **1**  |     0.7 x 0.7     |   12.5 x 12.5    |      -       |         Rack         |    -    |
| **2**  |     0.7 x 0.7     |   12.5 x 12.5    |      -       |         Rack         |    -    |
| **3**  |     1.0 x 0.8     |  17.86 x 14.29   |    255.22    | 255.22 / 10 = 25.522 |   52    |
| **4**  |     1.0 x 0.8     |  17.86 x 14.29   |    255.22    | 255.22 / 10 = 25.522 |   52    |
| **5**  |    1.25 x 0.8     |  22.32 x 14.29   |    318.95    | 318.95 / 10 = 31.895 |   64    |
| **6**  |    0.8 x 1.60     |  14.29 x 28.57   |    408.27    | 408.27 / 10 = 40.827 |   82    |
| **7**  |    1.45 x 0.9     |   25.5 x 16.1    |    410.55    | 410.55 / 10 = 41.055 |   82    |
| **8**  |    1.72 x 0.8     |   30.7 x 14.29   |    439.01    | 439.01 / 10 = 43.901 |   88    |
| **9**  |    0.84 x 0.8     |    15 x 14.29    |    214.5     |  214.5 / 10 = 21.45  |   44    |
| **10** |    1.77 x 0.8     |   31.6 x 14.29   |    451.88    | 451.88 / 10 = 45.188 |   92    |
| **11** |     2.4 x 0.8     |   42.8 x 14.29   |    612.04    | 612.04 / 10 = 61.204 |   124   |
| **12** |    1.92 x 0.8     |   34.3 x 14.29   |    490.49    | 490.49 / 10 = 49.049 |   100   |
| **13** |    1.25 x 0.8     |   22.3 x 14.29   |    318.89    | 318.89 / 10 = 31.889 |   64    |
| **14** |    1.15 x 0.8     |   20.5 x 14.29   |    293.15    | 293.15 / 10 = 29.315 |   60    |
| **15** |     2.1 x 0.8     |   37.5 x 14.29   |    536.25    | 536.25 / 10 = 53.625 |   108   |
| **16** |    0.8 x 1.65     |   14.29 x 29.5   |    421.85    | 421.85 / 10 = 42.185 |   86    |
| **17** |     1.4 x 0.9     |    25 x 16.1     |    402.5     |  402.5 / 10 = 40.2   |   82    |
| **22** |    0.8 x 0.65     |   14.29 x 11.6   |      -       |         Rack         |    -    |
| **23** |     1.9 x 0.8     |   33.9 x 14.29   |    484.77    | 484.77 / 10 = 48.477 |   98    |
| **24** |     2.2 x 0.8     |   39.3 x 14.3    |    561.99    | 561.99 / 10 = 56.199 |   114   |
| **25** |     0.8 x 1.6     |   14.29 x 28.6   |    408.69    | 408.69 / 10 = 40.869 |   82    |
| **26** |     0.8 x 0.8     |  14.29 x 14.29   |      -       |         Rack         |    -    |


**Total Standard Outlets for Level 2: 1474**

---

### 2.2.1. External Wall (Level 2 Only)

According to the specifications, installation of a network outlet (ISO 8877) is required every 5 meters along the right
exterior wall and the upper exterior wall.

* **Upper Exterior Wall:** 150 / 5 = 30 outlets
* **Right Exterior Wall:** 400 / 5 = 80 outlets
* **Total External Outlets:** 110 outlets