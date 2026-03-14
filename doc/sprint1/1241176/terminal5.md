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

---

## 3. Access Points

> Both floors require LAN coverage (Wi-Fi)

> Each Access Point covers a circle of $50m$ diameter

> All APs will be installed in the space above the dropped ceiling

> Each AP will require **a dedicated outlet**

> All APs on this terminal will operate on **5GHz band**, since this band offers a much larger number of available
channels, and it also has **DFS (Dynamic Frequency Selection)**, which selects a channel in order avoid interference
with it's neighbours.


### 3.1. Calc Methology
We will use the diagonal check for rooms and the density formula for open areas:

* **Single Coverage Condition:** $$D_r = \sqrt{length^2 + width^2} \leq D_c = 2 \times radius = 50 meters\ $$

* **Calculation for Wide Areas:** If $D_r \ge 50 meters\ $, then $$ n_{APs} = \lceil (L-2c)/(2c) \rceil + 2 $$

---

#### 3.1.1. Level 0 Rooms

| ROOMS  | $D_r = \sqrt{length^2 + width^2} $ (m) | $D_r \leq 50 meters$? | TOTAL APs |
|:------:|:--------------------------------------:|:---------------------:|:---------:|
| **1**  |    $\sqrt{12.5^2 + 12.5^2} = 17.68$    |          Yes          |     1     |
| **2**  |    $\sqrt{12.5^2 + 12.5^2} = 17.68$    |          Yes          |     1     |
| **3**  |    $\sqrt{39.3^2 + 14.3^2} = 41.82$    |          Yes          |     1     |
| **4**  |    $\sqrt{22.2^2 + 14.3^2} = 26.41$    |          Yes          |     1     |
| **5**  |    $\sqrt{22.3^2 + 14.3^2} = 26.50$    |          Yes          |     1     |
| **6**  |    $\sqrt{34.8^2 + 14.3^2} = 37.62$    |          Yes          |     1     |
| **7**  |    $\sqrt{19.6^2 + 14.3^2} = 24.26$    |          Yes          |     1     |
| **8**  |    $\sqrt{34.8^2 + 14.3^2} = 37.62$    |          Yes          |     1     |
| **9**  |    $\sqrt{22.2^2 + 14.3^2} = 26.41$    |          Yes          |     1     |
| **10** |    $\sqrt{14.3^2 + 30.5^2} = 33.68$    |          Yes          |     1     |
| **11** |    $\sqrt{12.5^2 + 30.5^2} = 32.96$    |          Yes          |     1     |
| **12** |    $\sqrt{12.5^2 + 30.5^2} = 30.96$    |          Yes          |     1     |
| **13** |    $\sqrt{12.5^2 + 30.5^2} = 30.96$    |          Yes          |     1     |
| **14** |    $\sqrt{14.3^2 + 28.6^2} = 31.98$    |          Yes          |     1     |
| **15** |    $\sqrt{25.0^2 + 16.1^2} = 29.73$    |          Yes          |     1     |
| **16** |    $\sqrt{28.6^2 + 14.3^2} = 31.98$    |          Yes          |     1     |
| **17** |    $\sqrt{25.0^2 + 14.3^2} = 28.80$    |          Yes          |     1     |
| **18** |    $\sqrt{12.5^2 + 11.6^2} = 17.05$    |          Yes          |     1     |
| **19** |    $\sqrt{33.9^2 + 14.3^2} = 36.79$    |          Yes          |     1     |
| **20** |    $\sqrt{40.2^2 + 14.3^2} = 42.66$    |          Yes          |     1     |
| **21** |    $\sqrt{28.6^2 + 14.3^2} = 31.98$    |          Yes          |     1     |
| **22** |    $\sqrt{12.5^2 + 11.6^2} = 17.05$    |          Yes          |     1     |

**Total APs for Level 0 rooms: 22 APs (Considering only rooms with standard outlets).**

#### 3.1.2. Level 0 Open Areas

Due to the large size of the T5 ($400m$ long), we will divide the open area into zones for greater accuracy.

| ZONE  | DIMENSIONS ($cm$) | DIMENSIONS ($m$) |    $n_{lines} = \lceil H/(2R) \rceil$     |     $y_i = H(2i - 1)/(2n_{lines})$     |    $d = min(y_i, H - y_i)$    |      $c = \sqrt{R² - d²}$       | $D_r$  |        $n_{APs} = \lceil (L-2c)/(2c) \rceil + 2 $        | TOTAL APs |
|:-----:|:-----------------:|:----------------:|:-----------------------------------------:|:--------------------------------------:|:-----------------------------:|:-------------------------------:|:------:|:--------------------------------------------------------:|:---------:|
| **A** |     1.5 x 0.8     |  26.19 x 14.29   | $n_{lines} = \lceil 14.29/50 \rceil = 1$  |  $\lceil (14.29(1))/2 \rceil = 7.15$   |   $\min(7.15, 7.14) = 7.15$   | $\sqrt{25^2 - 7.15^2} = 23.96$  | 29.83  | $\lceil \frac{26.19 - 47.92}{47.92} \rceil \!+\! 2 = 2$  |   **1**   |
| **B** |     5.7 x 0.8     |  101.79 x 14.29  | $n_{lines} = \lceil 14.29/50 \rceil = 1$  |  $\lceil (14.29(1))/2 \rceil = 7.15$   |   $\min(7.15, 7.14) = 7.15$   | $\sqrt{25^2 - 7.15^2} = 23.96$  | 102.79 | $\lceil \frac{101.79 - 47.92}{47.92} \rceil \!+\! 2 = 3$ |   **3**   |
| **C** |     6.4 x 9.0     | 114.29 x 160.71  | $n_{lines} = \lceil 160.71/50 \rceil = 4$ | $\lceil (160.71(1))/8 \rceil = 20.09$  | $\min(20.09, 140.62) = 20.09$ | $\sqrt{25^2 - 20.09^2} = 14.88$ | 197.21 | $\lceil \frac{114.29 - 29.76}{29.76} \rceil \!+\! 2 = 5$ |  **20**   |
| **D** |    1.4 x 19.3     |  25.00 x 344.64  | $n_{lines} = \lceil 344.64/50 \rceil = 7$ | $\lceil (344.64(1))/14 \rceil = 24.62$ | $\min(24.62, 320.02) = 24.62$ | $\sqrt{25^2 - 24.62^2} = 4.34$  | 345.55 |  $\lceil \frac{25.00 - 8.68}{8.68} \rceil \!+\! 2 = 4$   |  **28**   |
| **E** |     0.5 x 1.7     |   8.93 x 30.36   | $n_{lines} = \lceil 30.36/50 \rceil = 1$  |  $\lceil (30.36(1))/2 \rceil = 15.18$  | $\min(15.18, 15.18) = 15.18$  | $\sqrt{25^2 - 15.18^2} = 19.87$ | 31.65  |  $\lceil \frac{8.93 - 39.74}{39.74} \rceil \!+\! 2 = 1$  |   **1**   |
| **F** |     1.8 x 1.4     |  32.14 x 25.00   |   $n_{lines} = \lceil 25/50 \rceil = 1$   |   $\lceil (25(1))/2 \rceil = 12.50$    | $\min(12.50, 12.50) = 12.50$  | $\sqrt{25^2 - 12.50^2} = 21.65$ | 25.63  | $\lceil \frac{32.14 - 43.30}{43.30} \rceil \!+\! 2 = 2$  |   **1**   |
| **G** |     5.4 x 4.6     |  96.43 x 82.14   | $n_{lines} = \lceil 82.14/50 \rceil = 2$  |  $\lceil (82.14(1))/4 \rceil = 20.54$  | $\min(20.54, 61.60) = 20.54$  | $\sqrt{25^2 - 20.54^2} = 14.25$ | 126.67 | $\lceil \frac{96.43 - 28.50}{28.50} \rceil \!+\! 2 = 5$  |  **10**   |
| **H** |     2.2 x 3.3     |  39.29 x 58.93   | $n_{lines} = \lceil 58.93/50 \rceil = 2$  |  $\lceil (58.93(1))/4 \rceil = 14.73$  |  $\min(14.73, 44.2) = 14.73$  | $\sqrt{25^2 - 14.73^2} = 20.20$ | 70.83  | $\lceil \frac{39.29 - 40.40}{40.40} \rceil \!+\! 2 = 2$  |   **2**   |
| **I** |     1.9 x 0.9     |  33.93 x 16.07   | $n_{lines} = \lceil 16.07/50 \rceil = 1$  |  $\lceil (16.07(1))/2 \rceil = 8.04$   |   $\min(8.04, 8.03) = 8.04$   | $\sqrt{25^2 - 8.04^2} = 23.67$  | 37.54  | $\lceil \frac{33.93 - 47.34}{47.34} \rceil \!+\! 2 = 2$  |   **1**   |
| **J** |     1.6 x 2.6     |  28.57 x 46.43   | $n_{lines} = \lceil 46.43/50 \rceil = 1$  |  $\lceil (46.43(1))/2 \rceil = 23.22$  | $\min(23.22, 23.21) = 23.22$  | $\sqrt{25^2 - 23.22^2} = 9.27$  | 54.52  | $\lceil \frac{28.57 - 18.54}{18.54} \rceil \!+\! 2 = 3$  |   **3**   |
| **K** |     2.3 x 3.3     |  41.07 x 58.93   | $n_{lines} = \lceil 58.93/50 \rceil = 2$  |  $\lceil (58.93(1))/4 \rceil = 14.73$  |  $\min(14.73, 44.2) = 14.73$  | $\sqrt{25^2 - 14.73^2} = 20.20$ | 71.83  | $\lceil \frac{41.07 - 40.40}{40.40} \rceil \!+\! 2 = 2$  |   **2**   |
| **L** |     7.1 x 4.5     |  126.79 x 80.36  | $n_{lines} = \lceil 80.36/50 \rceil = 2$  |  $\lceil (80.36(1))/4 \rceil = 20.09$  | $\min(20.09, 60.27) = 20.09$  | $\sqrt{25^2 - 20.09^2} = 14.88$ | 150.11 | $\lceil \frac{126.79 - 29.76}{29.76} \rceil \!+\! 2 = 6$ |  **12**   |
| **M** |     1.6 x 0.8     |  28.57 x 14.29   | $n_{lines} = \lceil 14.29/50 \rceil = 1$  |  $\lceil (14.29(1))/2 \rceil = 7.15$   |   $\min(7.15, 7.14) = 7.15$   | $\sqrt{25^2 - 7.15^2} = 23.96$  | 31.94  | $\lceil \frac{28.57 - 47.92}{47.92} \rceil \!+\! 2 = 2$  |   **1**   |


**Estimated Total for Open Areas of Level 0: 85 APs**

*\*Note: All AP installations must be done in the false ceiling space (4 meters high), using the **5 GHz** band to maximize
interference.*

---

#### Summary of APs in Level 0

* APs in rooms: **22**
* APs in open areas: **85**
* **TOTAL: 107 Access Points**

---

#### 3.2. Level 2 Rooms

| ROOMS  | $D_r = \sqrt{length^2 + width^2} $ (m) | $D_r \leq 50 meters$? | TOTAL APs |
|:------:|:--------------------------------------:|:---------------------:|:---------:|
| **1**  |    $\sqrt{12.5^2 + 12.5^2} = 17.68$    |          Yes          |     1     |
| **2**  |    $\sqrt{12.5^2 + 12.5^2} = 17.68$    |          Yes          |     1     |
| **3**  |   $\sqrt{17.86^2 + 14.29^2} = 22.87$   |          Yes          |     1     |
| **4**  |   $\sqrt{17.86^2 + 14.29^2} = 22.87$   |          Yes          |     1     |
| **5**  |   $\sqrt{22.32^2 + 14.29^2} = 26.50$   |          Yes          |     1     |
| **6**  |   $\sqrt{14.29^2 + 28.57^2} = 31.94$   |          Yes          |     1     |
| **7**  |   $\sqrt{25.50^2 + 16.10^2} = 30.16$   |          Yes          |     1     |
| **8**  |   $\sqrt{30.70^2 + 14.29^2} = 33.86$   |          Yes          |     1     |
| **9**  |   $\sqrt{15.00^2 + 14.29^2} = 20.72$   |          Yes          |     1     |
| **10** |   $\sqrt{31.60^2 + 14.29^2} = 34.68$   |          Yes          |     1     |
| **11** |   $\sqrt{42.80^2 + 14.29^2} = 45.12$   |          Yes          |     1     |
| **12** |   $\sqrt{34.30^2 + 14.29^2} = 37.16$   |          Yes          |     1     |
| **13** |   $\sqrt{22.30^2 + 14.29^2} = 26.49$   |          Yes          |     1     |
| **14** |   $\sqrt{20.50^2 + 14.29^2} = 24.99$   |          Yes          |     1     |
| **15** |   $\sqrt{37.50^2 + 14.29^2} = 40.13$   |          Yes          |     1     |
| **16** |   $\sqrt{14.29^2 + 29.50^2} = 32.78$   |          Yes          |     1     |
| **17** |   $\sqrt{25.00^2 + 16.10^2} = 29.74$   |          Yes          |     1     |
| **18** |   $\sqrt{28.6^2 + 14.29^2} = 29.74$    |          Yes          |     1     |
| **19** |   $\sqrt{14.29^2 + 25.00^2} = 28.8$    |          Yes          |     1     |
| **20** |   $\sqrt{14.29^2 + 30.4^2} = 33.59$    |          Yes          |     1     |
| **21** |   $\sqrt{14.29^2 + 30.4^2} = 33.59$    |          Yes          |     1     |
| **22** |   $\sqrt{14.29^2 + 11.60^2} = 18.41$   |          Yes          |     1     |
| **23** |   $\sqrt{33.90^2 + 14.29^2} = 36.79$   |          Yes          |     1     |
| **24** |   $\sqrt{39.30^2 + 14.29^2} = 41.82$   |          Yes          |     1     |
| **25** |   $\sqrt{14.29^2 + 28.60^2} = 31.97$   |          Yes          |     1     |
| **26** |   $\sqrt{14.29^2 + 14.29^2} = 20.21$   |          Yes          |     1     |

**Total APs for Level 2 rooms: 26 APs (Considering only rooms with standard outlets).**

#### 3.2.1. Level 2 Open Areas

Due to the large size of the T5 ($400m$ long), we will divide the open area into zones for greater accuracy.

| ZONE  | DIMENSIONS ($cm$) | DIEMENSIONS ($m$) |    $n_{lines} = \lceil H/(2R) \rceil$     |     $y_i = H(2i - 1)/(2n_{lines})$     |    $d = min(y_i, H - y_i)$    |      $c = \sqrt{R² - d²}$       |  $D_r$   |         $n_{APs} = \lceil (L-2c)/(2c) \rceil + 2$         | TOTAL  |
|:-----:|:-----------------:|:-----------------:|:-----------------------------------------:|:--------------------------------------:|:-----------------------------:|:-------------------------------:|:--------:|:---------------------------------------------------------:|:------:|
| **A** |     3.2 x 0.8     |  $57.14 x 14.29$  | $n_{lines} = \lceil 14.29/50 \rceil = 1$  |  $\lceil (14.29(1))/2 \rceil = 7.15$   |   $\min(7.15, 7.14) = 7.15$   | $\sqrt{25^2 - 7.15^2} = 23.96$  | $58.90$  |  $\lceil \frac{57.14 - 47.92}{47.92} \rceil \!+\! 2 = 3$  | **3**  |
| **B** |     5.6 x 0.8     | $100.00 x 14.29$  | $n_{lines} = \lceil 14.29/50 \rceil = 1$  |  $\lceil (14.29(1))/2 \rceil = 7.15$   |   $\min(7.15, 7.14) = 7.15$   | $\sqrt{25^2 - 7.15^2} = 23.96$  | $101.02$ | $\lceil \frac{100.00 - 47.92}{47.92} \rceil \!+\! 2 = 4$  | **4**  |
| **C** |     2.7 x 1.8     |  $48.21 x 32.14$  | $n_{lines} = \lceil 32.14/50 \rceil = 1$  |  $\lceil (32.14(1))/2 \rceil = 16.07$  | $\min(16.07, 16.07) = 16.07$  | $\sqrt{25^2 - 16.07^2} = 19.15$ | $57.94$  |  $\lceil \frac{48.21 - 38.30}{38.30} \rceil \!+\! 2 = 3$  | **3**  |
| **D** |     1.6 x 1.9     |  $28.57 x 33.93$  | $n_{lines} = \lceil 33.93/50 \rceil = 1$  |  $\lceil (33.93(1))/2 \rceil = 16.97$  | $\min(16.97, 16.96) = 16.97$  | $\sqrt{25^2 - 16.97^2} = 18.36$ | $44.36$  |  $\lceil \frac{28.57 - 36.72}{36.72} \rceil \!+\! 2 = 2$  | **1**  |
| **E** |     0.9 x 1.3     |  $16.07 x 23.21$  | $n_{lines} = \lceil 23.21/50 \rceil = 1$  |  $\lceil (23.21(1))/2 \rceil = 11.61$  | $\min(11.61, 11.60) = 11.61$  | $\sqrt{25^2 - 11.61^2} = 22.13$ | $28.23$  |  $\lceil \frac{16.07 - 44.26}{44.26} \rceil \!+\! 2 = 2$  | **1**  |
| **F** |     2.0 x 2.2     |  $35.71 x 39.29$  | $n_{lines} = \lceil 39.29/50 \rceil = 1$  |  $\lceil (39.29(1))/2 \rceil = 19.65$  | $\min(19.65, 19.64) = 19.65$  | $\sqrt{25^2 - 19.65^2} = 15.45$ | $53.09$  |  $\lceil \frac{35.71 - 30.90}{30.90} \rceil \!+\! 2 = 3$  | **3**  |
| **G** |    15.1 x 1.2     | $269.64 x 21.43$  | $n_{lines} = \lceil 21.43/50 \rceil = 1$  |  $\lceil (21.43(1))/2 \rceil = 10.72$  | $\min(10.72, 10.71) = 10.72$  | $\sqrt{25^2 - 10.72^2} = 22.58$ | $270.49$ | $\lceil \frac{269.64 - 45.16}{45.16} \rceil \!+\! 2 = 7$  | **7**  |
| **H** |    4.5 x 15.1     | $80.36 x 269.64$  | $n_{lines} = \lceil 269.64/50 \rceil = 6$ | $\lceil (269.64(1))/12 \rceil = 22.47$ | $\min(22.47, 247.17) = 22.47$ | $\sqrt{25^2 - 22.47^2} = 10.96$ | $281.36$ |  $\lceil \frac{80.36 - 21.92}{21.92} \rceil \!+\! 2 = 5$  | **30** |
| **I** |     2.9 x 0.6     |  $51.79 x 10.71$  | $n_{lines} = \lceil 10.71/50 \rceil = 1$  |  $\lceil (10.71(1))/2 \rceil = 5.36$   |   $\min(5.36, 5.35) = 5.36$   | $\sqrt{25^2 - 5.36^2} = 24.42$  | $52.89$  |  $\lceil \frac{51.79 - 48.84}{48.84} \rceil \!+\! 2 = 3$  | **3**  |
| **J** |     1.4 x 2.2     |  $25.00 x 39.29$  | $n_{lines} = \lceil 39.29/50 \rceil = 1$  |  $\lceil (39.29(1))/2 \rceil = 19.65$  | $\min(19.65, 19.64) = 19.65$  | $\sqrt{25^2 - 19.65^2} = 15.45$ | $46.57$  |  $\lceil \frac{25.00 - 30.90}{30.90} \rceil \!+\! 2 = 2$  | **1**  |
| **K** |     1.3 x 1.2     |  $23.21 x 21.43$  | $n_{lines} = \lceil 21.43/50 \rceil = 1$  |  $\lceil (21.43(1))/2 \rceil = 10.72$  | $\min(10.72, 10.71) = 10.72$  | $\sqrt{25^2 - 10.72^2} = 22.58$ | $31.59$  |  $\lceil \frac{23.21 - 45.16}{45.16} \rceil \!+\! 2 = 2$  | **1**  |
| **L** |       1 x 1       |  $17.86 x 17.86$  | $n_{lines} = \lceil 17.86/50 \rceil = 1$  |  $\lceil (17.86(1))/2 \rceil = 8.93$   |   $\min(8.93, 8.93) = 8.93$   | $\sqrt{25^2 - 8.93^2} = 23.35$  | $25.26$  |  $\lceil \frac{17.86 - 46.70}{46.70} \rceil \!+\! 2 = 2$  | **1**  |
| **M** |     5.4 x 2.1     |  $96.43 x 37.50$  | $n_{lines} = \lceil 37.50/50 \rceil = 1$  |  $\lceil (37.50(1))/2 \rceil = 18.75$  | $\min(18.75, 18.75) = 18.75$  | $\sqrt{25^2 - 18.75^2} = 16.54$ | $103.46$ |  $\lceil \frac{96.43 - 33.08}{33.08} \rceil \!+\! 2 = 4$  | **4**  |
| **N** |     1.6 x 0.8     |  $28.57 x 14.29$  | $n_{lines} = \lceil 14.29/50 \rceil = 1$  |  $\lceil (14.29(1))/2 \rceil = 7.15$   |   $\min(7.15, 7.14) = 7.15$   | $\sqrt{25^2 - 7.15^2} = 23.96$  | $31.94$  |  $\lceil \frac{28.57 - 47.92}{47.92} \rceil \!+\! 2 = 2$  | **1**  |
| **O** |    1.5 x 19.7     | $26.79 x 351.79$  | $n_{lines} = \lceil 351.79/50 \rceil = 8$ | $\lceil (351.79(1))/16 \rceil = 21.99$ | $\min(21.99, 329.80) = 21.99$ | $\sqrt{25^2 - 21.99^2} = 11.90$ | $352.81$ |  $\lceil \frac{26.79 - 23.80}{23.80} \rceil \!+\! 2 = 3$  | **24** |

*\*Note about Zones H and O: DDue to the high height/length in these zones, multiple coverage lines ($n_{lines}$) were
calculated. For Zone H, with 6 lines and a horizontal distribution of 5 APs per line, we total 30 units to ensure
there are no dead zones.*

**Estimated Total for Open Areas: 87 APs**

---

#### Summary of APs in Level 2

* APs in rooms: **26**
* APs in open areas: **87**
* **TOTAL: 113 Access Points**