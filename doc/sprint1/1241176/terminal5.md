# RCOMP 2025-2026: Project 1 Sprint 1 Member 1221176 File
=====

# Contents

1. [Scale and Measurements](#1-scale-and-measurements)

2. [Network Outlets Calculation](#2-network-outlets-calculation)
    - [Level 0 (Arrivals)](#21-level-0-arrivals)
    - [Level 2 (Departures)](#22-level-2-departures)
      
3. [Access Points Calculation](#3-access-points-calculation)
    - [Calc Methology](#31-calc-methology)
        - [Level 0 Rooms](#311-level-0-rooms)
        - [Level 0 Open Areas](#312-level-0-open-areas)
    - [Level 2 Rooms](#32-level-2-rooms)
        - [Level 2 Open Areas](#321-level-2-open-areas)
    - [Hardware Summary](#33-hardware-summary)

4. [Cross Connects](#4-cross-connects)
    - [Cross Connects Calculation](#41-cross-connects-calculation)
        - [Level 0 (Arrivals)](#411-level-0-arrivals)
        - [Level 2 (Departures)](#412-level-2-departures)

5. [Cable Pathways](#5-cable-pathways)
    - [Cable Pathways Calculation](#51-cable-pathways-calculation)
        - [Level 0 (Arrivals)](#511-level-0-arrivals)
        - [Level 2 (Departures)](#512-level-2-departures)

6. [Hardware Inventory](#6-hardware-inventory)
    - [Access Points & DO](#61-access-points-and-dedicated-outlets)

---

# Terminal 5

## 1. Scale and Measurements

* **Building Dimensions:** $400m × 150m = 60 000m²$
* **Scale Used:** $2.8cm <=> 50m -> 1cm ⇔ 17.86m$
* **Floor Specifications:** Ceiling height is $5m$, with a dropped ceiling at $4m$ from the ground, covering the entire 
floor (perfect for installing cable raceways and wireless access points).

---

## 2. Network Outlets Calculation

**Standard Rule:** Two outlets per 10m² of work area (`outlets = Work Area * 2`)
* **NOTE:** `Work Area = room area / 10`

---

## 2.1. Level 0 (Arrivals)

> Rooms **WITH** Standard Outlets: 3, 4, 5, 6, 7, 8, 9, 10, 11, 14, 15, 19, 20, and 21.

> Rooms **WITHOUT** Outlets: 1, 2, 12, 13, 16, 17, 18, and 22.

> Rooms for **Hardware:** 1, 2, 18, and 22

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

This schematic shows an example layout for the outlets on the Level. The plan is not drawn to scale, as doing so would 
make the diagram too difficult to read. When placing the outlets, no point in each room can be more than 3 meters away 
from one.

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
| **13** |     2.2 x 0.8     |  39.29 x 14.29   |    561.45    | 561.45 / 10 = 56.145 |   112   |
| **14** |    1.15 x 0.8     |   20.5 x 14.29   |    293.15    | 293.15 / 10 = 29.315 |   60    |
| **15** |     2.1 x 0.8     |   37.5 x 14.29   |    536.25    | 536.25 / 10 = 53.625 |   108   |
| **16** |    0.8 x 1.65     |   14.29 x 29.5   |    421.85    | 421.85 / 10 = 42.185 |   86    |
| **17** |     1.4 x 0.9     |    25 x 16.1     |    402.5     |  402.5 / 10 = 40.2   |   82    |
| **22** |    0.8 x 0.65     |   14.29 x 11.6   |      -       |         Rack         |    -    |
| **23** |     1.9 x 0.8     |   33.9 x 14.29   |    484.77    | 484.77 / 10 = 48.477 |   98    |
| **24** |     2.2 x 0.8     |   39.3 x 14.3    |    561.99    | 561.99 / 10 = 56.199 |   114   |
| **25** |     0.8 x 1.6     |   14.29 x 28.6   |    408.69    | 408.69 / 10 = 40.869 |   82    |
| **26** |     0.8 x 0.8     |  14.29 x 14.29   |      -       |         Rack         |    -    |


**Total Standard Outlets for Level 2: 1522**

---

#### Schematic Plan (For Standard Outlets Only)

This schematic shows an example layout for the outlets on the Level. The plan **is not** drawn to scale, as doing so
would make the diagram too difficult to read. When placing the outlets, no point in each room can be more than 3 meters 
away from one.

![Network Outlets Deployment Schematic Plan Level 0](doc/sprint1/1241176/assets/Terminal5_Lvl2_Outlets.svg)

**(For clarity, outlets associated with Access Points will be shown on a separate schematic)**

---

## 3. Access Points

> Both floors require LAN coverage (Wi-Fi)

> Each Access Point covers a circle of $50m$ diameter

> All APs will be installed in the space above the dropped ceiling

> Each AP will require **a dedicated outlet**

> All APs on this terminal will operate on **5GHz band**, since this band offers a much larger number of available
channels, and it also has **DFS (Dynamic Frequency Selection)**, which selects a channel in order avoid interference
with its neighbours.


### 3.1. Calc Methology
To calculate the number of access points required in a room we will utilize the following formulas:

- $$D_a = \sqrt{length^2 + width^2} \leq D_c $$
- $$D_c = 2 \times radius = 50 \ m$$
   - where $D_a$ is the diagonal of the area is the diagonal of the area we are calculating the access points for.
   - where $D_c$ is the diameter of an access point (50 $m$).

If $D_a \ge D_c$, we will require more than 1 access point. To calculate the exact amount and positions of access points needed in the room/area we utilize the following formulas:

- $$y_i = H(2i-1)/(2n_{lines})$$
   - where $y_i$ is the y coordinate of the line
   - where $H$ is the height of the area
   - where $i$ is the current line
   - where $n_{lines}$

- $$d = min(y_i, H - y_i)$$
   - where $d$ is the distance of the line to the horizontal wall
   - where $H$ is the height of the area
   - where $i$ is the current line
   - where $y_i$ is the y coordinate of the current line

- $$c = \sqrt{R² - d²}$$
   - where $c$ is the distance of the first access point to the vertical wall so that the area covers the corner
   - where $R = 25$
   - where $d$ is the distance of the line to the horizontal wall

- $$n_{lines} = \lceil H/(2R) \rceil$$
   - where $n_{lines}$ is the number of lines of access points and shall always be rounded **up**
   - where $H$ is the height of the area
   - where $R = 25 m$

- $$n_{APs} = \lfloor (L-2c)/(2c) \rfloor + 2$$
   - where $n_{APs}$ is the number of APs per line and shall always be rounded **up**
   - where $L$ is the length of the area
   - where $c$ is the distance of the first access point to the vertical wall so that the area covers the corner

- $$n_{Total} = \sum_{i=1}^{n_{lines}} n_{APs}$$
   - where $n_{Total}$ is the total of access points required in the room/area
   - where $n_{lines} is the number of lines of access points in the room/area
   - where $n_{APs} is the number of access points per line

- $$spacing = (L-2c)/(n_{APs}-1)$$
   - where $spacing$ is the distance between 2 access points
   - where $L$ is the length of the area
   - where $c$ is the distance of the first access point to the vertical wall so that the area covers the corner
   - where $n_{APs} is the number of APs per line

If the room/area only requires 1 access point, we can skip the calculation of $n_{lines}$ and $d = y_i$. The position of the access point will be the center of the room/area.

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

**Total APs for Level 0 rooms: 22 APs.**

#### 3.1.2. Level 0 Open Areas

Due to the large size of the T5 ($400m$ long), we will divide the open area into zones for greater accuracy.

| ZONE  | DIMENSIONS ($cm$) | DIMENSIONS ($m$) |    $n_{lines} = \lceil H/(2R) \rceil$     |    $y_i = H(2i - 1)/(2n_{lines})$     |    $d = min(y_i, H - y_i)$    |      $c = \sqrt{R² - d²}$       | $D_r$  |        $n_{APs} = \lceil (L-2c)/(2c) \rceil + 2 $        | TOTAL APs |
|:-----:|:-----------------:|:----------------:|:-----------------------------------------:|:-------------------------------------:|:-----------------------------:|:-------------------------------:|:------:|:--------------------------------------------------------:|:---------:|
| **A** |     1.5 x 0.8     |  26.19 x 14.29   | $n_{lines} = \lceil 14.29/50 \rceil = 1$  |  $\lceil (14.29(1))/2 \rceil = 7.15$  |   $\min(7.15, 7.14) = 7.15$   | $\sqrt{25^2 - 7.15^2} = 23.96$  | 29.83  | $\lceil \frac{26.19 - 47.92}{47.92} \rceil \!+\! 2 = 2$  |   **1**   |
| **B** |     5.7 x 0.8     |  101.79 x 14.29  | $n_{lines} = \lceil 14.29/50 \rceil = 1$  |  $\lceil (14.29(1))/2 \rceil = 7.15$  |   $\min(7.15, 7.14) = 7.15$   | $\sqrt{25^2 - 7.15^2} = 23.96$  | 102.79 | $\lceil \frac{101.79 - 47.92}{47.92} \rceil \!+\! 2 = 3$ |   **3**   |
| **C** |     6.4 x 9.0     | 114.29 x 160.71  | $n_{lines} = \lceil 160.71/50 \rceil = 4$ | $\lceil (160.71(1))/8 \rceil = 20.09$ | $\min(20.09, 140.62) = 20.09$ | $\sqrt{25^2 - 20.09^2} = 14.88$ | 197.21 | $\lceil \frac{114.29 - 29.76}{29.76} \rceil \!+\! 2 = 5$ |  **20**   |
| **D** |    1.4 x 19.3     |  25.00 x 344.64  | $n_{lines} = \lceil 25.00/50 \rceil = 1$  |   $\lceil (25(1))/2 \rceil = 12.50$   | $\min(12.50, 12.50) = 12.50$  | $\sqrt{25^2 - 12.50^2} = 21.65$ | 345.55 | $\lceil \frac{344.64 - 43.30}{43.30} \rceil \!+\| 2 = 9$ |   **9**   |
| **E** |     0.5 x 1.7     |   8.93 x 30.36   | $n_{lines} = \lceil 30.36/50 \rceil = 1$  | $\lceil (30.36(1))/2 \rceil = 15.18$  | $\min(15.18, 15.18) = 15.18$  | $\sqrt{25^2 - 15.18^2} = 19.87$ | 31.65  |  $\lceil \frac{8.93 - 39.74}{39.74} \rceil \!+\! 2 = 1$  |   **1**   |
| **F** |     1.8 x 1.4     |  32.14 x 25.00   |   $n_{lines} = \lceil 25/50 \rceil = 1$   |   $\lceil (25(1))/2 \rceil = 12.50$   | $\min(12.50, 12.50) = 12.50$  | $\sqrt{25^2 - 12.50^2} = 21.65$ | 25.63  | $\lceil \frac{32.14 - 43.30}{43.30} \rceil \!+\! 2 = 2$  |   **1**   |
| **G** |     5.4 x 4.6     |  96.43 x 82.14   | $n_{lines} = \lceil 82.14/50 \rceil = 2$  | $\lceil (82.14(1))/4 \rceil = 20.54$  | $\min(20.54, 61.60) = 20.54$  | $\sqrt{25^2 - 20.54^2} = 14.25$ | 126.67 | $\lceil \frac{96.43 - 28.50}{28.50} \rceil \!+\! 2 = 5$  |  **10**   |
| **H** |     2.2 x 3.3     |  39.29 x 58.93   | $n_{lines} = \lceil 58.93/50 \rceil = 2$  | $\lceil (58.93(1))/4 \rceil = 14.73$  |  $\min(14.73, 44.2) = 14.73$  | $\sqrt{25^2 - 14.73^2} = 20.20$ | 70.83  | $\lceil \frac{39.29 - 40.40}{40.40} \rceil \!+\! 2 = 2$  |   **2**   |
| **I** |     1.9 x 0.9     |  33.93 x 16.07   | $n_{lines} = \lceil 16.07/50 \rceil = 1$  |  $\lceil (16.07(1))/2 \rceil = 8.04$  |   $\min(8.04, 8.03) = 8.04$   | $\sqrt{25^2 - 8.04^2} = 23.67$  | 37.54  | $\lceil \frac{33.93 - 47.34}{47.34} \rceil \!+\! 2 = 2$  |   **1**   |
| **J** |     1.6 x 2.6     |  28.57 x 46.43   | $n_{lines} = \lceil 46.43/50 \rceil = 1$  | $\lceil (46.43(1))/2 \rceil = 23.22$  | $\min(23.22, 23.21) = 23.22$  | $\sqrt{25^2 - 23.22^2} = 9.27$  | 54.52  | $\lceil \frac{28.57 - 18.54}{18.54} \rceil \!+\! 2 = 3$  |   **3**   |
| **K** |     2.3 x 3.3     |  41.07 x 58.93   | $n_{lines} = \lceil 58.93/50 \rceil = 2$  | $\lceil (58.93(1))/4 \rceil = 14.73$  |  $\min(14.73, 44.2) = 14.73$  | $\sqrt{25^2 - 14.73^2} = 20.20$ | 71.83  | $\lceil \frac{41.07 - 40.40}{40.40} \rceil \!+\! 2 = 2$  |   **2**   |
| **L** |     7.1 x 4.5     |  126.79 x 80.36  | $n_{lines} = \lceil 80.36/50 \rceil = 2$  | $\lceil (80.36(1))/4 \rceil = 20.09$  | $\min(20.09, 60.27) = 20.09$  | $\sqrt{25^2 - 20.09^2} = 14.88$ | 150.11 | $\lceil \frac{126.79 - 29.76}{29.76} \rceil \!+\! 2 = 6$ |  **12**   |
| **M** |     1.6 x 0.8     |  28.57 x 14.29   | $n_{lines} = \lceil 14.29/50 \rceil = 1$  |  $\lceil (14.29(1))/2 \rceil = 7.15$  |   $\min(7.15, 7.14) = 7.15$   | $\sqrt{25^2 - 7.15^2} = 23.96$  | 31.94  | $\lceil \frac{28.57 - 47.92}{47.92} \rceil \!+\! 2 = 2$  |   **1**   |


**Estimated Total for Open Areas of Level 0: 66 APs**

*\*Note: All AP installations must be done in the false ceiling space (4 meters high), using the **5 GHz** band to maximize
interference.*


#### Schematic Plan (For APs and Dedicated Outlets)
> This schematic shows how to place the APs and their Dedicated Outlets.

|            Access Points Schematic LEVEL 0 (AP Location + Dedicated Outlets)            |     Access Points Schematic LEVEL 0 (AP Area Coverage + Dedicated Outlets)      |
|:---------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| ![Access Points Schematic](doc/sprint1/1241176/assets/Terminal5_Level0-APs-SemArea.svg) | ![Access Points Schematic](doc/sprint1/1241176/assets/Terminal5_Level0-APs.svg) |


---

#### Summary of APs in Level 0

* APs in rooms: **22**
* APs in open areas: **66**
* **TOTAL: 88 Access Points**

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

**Total APs for Level 2 rooms: 26 APs.**

#### 3.2.1. Level 2 Open Areas

Due to the large size of the T5 ($400m$ long), we will divide the open area into zones for greater accuracy.

| ZONE  | DIMENSIONS ($cm$) | DIEMENSIONS ($m$) |              $n_{lines} = \lceil H/(2R) \rceil$               |     $y_i = H(2i - 1)/(2n_{lines})$     |    $d = min(y_i, H - y_i)$    |      $c = \sqrt{R² - d²}$       |  $D_r$   |               $n_{APs} = \lceil (L-2c)/(2c) \rceil + 2$               | TOTAL  |
|:-----:|:-----------------:|:-----------------:|:-------------------------------------------------------------:|:--------------------------------------:|:-----------------------------:|:-------------------------------:|:--------:|:---------------------------------------------------------------------:|:------:|
| **A** |     1.8 x 0.8     |   32.14 x 14.29   |           $n_{lines} = \lceil 14.29/50 \rceil = 1$            |  $\lceil (14.29(1))/2 \rceil = 7.15$   |   $\min(7.15, 7.14) = 7.15$   | $\sqrt{25^2 - 7.15^2} = 23.96$  | $35.17$  | $\lceil \frac{57.14 - 47.92}{47.92} \rceil \!+\! 2 = 3$ ($D_r < 50m$) | **1**  |
| **B** |     5.6 x 0.8     |  100.00 x 14.29   |           $n_{lines} = \lceil 14.29/50 \rceil = 1$            |  $\lceil (14.29(1))/2 \rceil = 7.15$   |   $\min(7.15, 7.14) = 7.15$   | $\sqrt{25^2 - 7.15^2} = 23.96$  | $101.02$ |       $\lceil \frac{100.00 - 47.92}{47.92} \rceil \!+\! 2 = 3$        | **3**  |
| **C** |     2.7 x 1.8     |   48.21 x 32.14   |           $n_{lines} = \lceil 48.21/50 \rceil = 1$            |  $\lceil (48.21(1))/2 \rceil = 24.11$  | $\min(24.11, 24.10) = 24.10$  | $\sqrt{25^2 - 16.07^2} = 6.65$  | $57.94$  |        $\lceil \frac{32.14 - 13.30}{13.30} \rceil \!+\! 2 = 2$        | **2**  |
| **D** |     1.6 x 1.9     |   28.57 x 33.93   |           $n_{lines} = \lceil 33.93/50 \rceil = 1$            |  $\lceil (33.93(1))/2 \rceil = 16.97$  | $\min(16.97, 16.96) = 16.97$  | $\sqrt{25^2 - 16.97^2} = 18.36$ | $44.36$  |        $\lceil \frac{28.57 - 36.72}{36.72} \rceil \!+\! 2 = 2$        | **1**  |
| **E** |     0.9 x 1.3     |   16.07 x 23.21   |           $n_{lines} = \lceil 23.21/50 \rceil = 1$            |  $\lceil (23.21(1))/2 \rceil = 11.61$  | $\min(11.61, 11.60) = 11.61$  | $\sqrt{25^2 - 11.61^2} = 22.13$ | $28.23$  |        $\lceil \frac{16.07 - 44.26}{44.26} \rceil \!+\! 2 = 2$        | **1**  |
| **F** |     2.0 x 2.2     |   35.71 x 39.29   |           $n_{lines} = \lceil 39.29/50 \rceil = 1$            |  $\lceil (39.29(1))/2 \rceil = 19.65$  | $\min(19.65, 19.64) = 19.65$  | $\sqrt{25^2 - 19.65^2} = 15.45$ | $53.09$  |        $\lceil \frac{35.71 - 30.90}{30.90} \rceil \!+\! 2 = 2$        | **2**  |
| **G** |    15.1 x 1.2     |   269.64 x 21.4   | $n_{lines} = \lceil 269.64/50 \rceil = 6$ (One vertical line) |   $\lceil (21.4(1))/2 \rceil = 10.7$   |  $\min(10.7, 10.7) = 10.70$   | $\sqrt{25^2 - 10.72^2} = 22.59$ | $270.49$ |       $\lceil \frac{269.64 - 45.16}{45.16} \rceil \!+\! 2 = 7$        | **7**  |
| **H** |    4.5 x 15.1     |  80.36 x 269.64   |           $n_{lines} = \lceil 269.64/50 \rceil = 6$           | $\lceil (269.64(1))/12 \rceil = 22.47$ | $\min(22.47, 247.17) = 22.47$ | $\sqrt{25^2 - 22.47^2} = 10.96$ | $281.36$ |        $\lceil \frac{80.36 - 21.92}{21.92} \rceil \!+\! 2 = 5$        | **30** |
| **I** |     2.9 x 0.6     |   51.79 x 10.71   |           $n_{lines} = \lceil 10.71/50 \rceil = 1$            |  $\lceil (10.71(1))/2 \rceil = 5.36$   |   $\min(5.36, 5.35) = 5.35$   | $\sqrt{25^2 - 5.35^2} = 24.42$  | $52.89$  |        $\lceil \frac{51.79 - 48.84}{48.84} \rceil \!+\! 2 = 2$        | **2**  |
| **J** |     1.4 x 2.2     |   25.00 x 39.29   |           $n_{lines} = \lceil 39.29/50 \rceil = 1$            |  $\lceil (39.29(1))/2 \rceil = 19.65$  | $\min(19.65, 19.64) = 19.65$  | $\sqrt{25^2 - 19.65^2} = 15.45$ | $46.57$  |        $\lceil \frac{25.00 - 30.90}{30.90} \rceil \!+\! 2 = 2$        | **1**  |
| **K** |     1.3 x 1.2     |   23.21 x 21.43   |           $n_{lines} = \lceil 21.43/50 \rceil = 1$            |  $\lceil (21.43(1))/2 \rceil = 10.72$  | $\min(10.72, 10.71) = 10.72$  | $\sqrt{25^2 - 10.72^2} = 22.58$ | $31.59$  |        $\lceil \frac{23.21 - 45.16}{45.16} \rceil \!+\! 2 = 2$        | **1**  |
| **L** |       1 x 1       |   17.86 x 17.86   |           $n_{lines} = \lceil 17.86/50 \rceil = 1$            |  $\lceil (17.86(1))/2 \rceil = 8.93$   |   $\min(8.93, 8.93) = 8.93$   | $\sqrt{25^2 - 8.93^2} = 23.35$  | $25.26$  |        $\lceil \frac{17.86 - 46.70}{46.70} \rceil \!+\! 2 = 2$        | **1**  |
| **M** |     5.4 x 2.1     |   96.43 x 37.50   |           $n_{lines} = \lceil 37.50/50 \rceil = 1$            |  $\lceil (37.50(1))/2 \rceil = 18.75$  | $\min(18.75, 18.75) = 18.75$  | $\sqrt{25^2 - 18.75^2} = 16.54$ | $103.46$ |        $\lceil \frac{96.43 - 33.08}{33.08} \rceil \!+\! 2 = 4$        | **4**  |
| **N** |     1.6 x 0.8     |   28.57 x 14.29   |           $n_{lines} = \lceil 14.29/50 \rceil = 1$            |  $\lceil (14.29(1))/2 \rceil = 7.15$   |   $\min(7.15, 7.14) = 7.15$   | $\sqrt{25^2 - 7.15^2} = 23.96$  | $31.94$  |        $\lceil \frac{28.57 - 47.92}{47.92} \rceil \!+\! 2 = 2$        | **1**  |
| **O** |    1.5 x 19.7     |  26.79 x 351.79   | $n_{lines} = \lceil 351.79/50 \rceil = 8$ (One vertical line) |  $\lceil (26.79(1))/2 \rceil = 13.40$  | $\min(13.40, 13.39) = 13.39$  | $\sqrt{25^2 - 13.40^2} = 21.11$ | $352.81$ |       $\lceil \frac{351.79 - 42.22}{42.22} \rceil \!+\! 2 = 10$       | **10** |

*\*Note about Zones H and O: Due to the high height/length in these zones, multiple coverage lines ($n_{lines}$) were
calculated. For Zone H, with 6 lines and a horizontal distribution of 5 APs per line, we total 30 units to ensure
there are no dead zones.*

**Estimated Total for Open Areas: 67 APs**

---

#### Summary of APs in Level 2

* APs in rooms: **26**
* APs in open areas: **67**
* **TOTAL: 93 Access Points**

---

#### Schematic Plan (For APs and Dedicated Outlets)
> This schematic shows how to place the APs and their Dedicated Outlets.

|            Access Points Schematic LEVEL 0 (AP Location + Dedicated Outlets)            |        Access Points Schematic LEVEL 0 (AP Area Coverage + Dedicated Outlets)        |
|:---------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| ![Access Points Schematic](doc/sprint1/1241176/assets/Terminal5_Lvl2_AP_DO.svg) | ![Access Points Schematic](doc/sprint1/1241176/assets/Terminal5_Lvl2_AP_DO_Area.svg) |


---

### 3.3. Hardware Summary

* **Total APs on Level 0:**  88 APs
* **Total APs on Level 2:** 93 APs
* **Dedicated Outlets:** Each AP requires an ISO 8877 dedicated outlet in the ceiling.

---


## 4. Cross Connections

> Each cable (whatever their type is) length should be less than 90 meters.

> Cables connecting an IC to a HC are limited to 500 meters long.

> Cables connecting an MC to an IC are limited to 1500 meters long.

> Each enclosure has a size of 42U, which means it allows 200 connections (1U must be free).

> There must be one IC per level.

> All HCs will be placed on the dropped ceiling.

---

### 4.1. Positioning of HCs

For the HCs, we will divide both levels of the terminal into zones to remove the need of consolidation points from the 
terminal, reducing the chances of a potential point of failure and ensuring no copper cable exceeds the 90m limit.

---
#### 4.1.1. Level 0 (Arrivals)

|    HC    |             POSITION              | ROOMS COVERED |       AREAS COVERED       | OUTLETS | APs | TOTAL CONNECTIONS |
|:--------:|:---------------------------------:|:-------------:|:-------------------------:|:-------:|:---:|:-----------------:|
| HC-L0-01 |              Room 1               |       3       |      Zone A, D (Top)      |   112   |  5  |      **117**      |
| HC-L0-02 |              Room 2               |       -       |   Zone B, C (Top Right)   |    0    |  8  |       **8**       |
| HC-L0-03 |   Zone D (Corridor, near R4-5)    |     4, 5      |     Zone D (Mid-Top)      |   138   |  5  |      **143**      |
| HC-L0-04 |   Zone D (Corridor, near R7-8)    |     7, 8      |    Zone D (Mid-Bottom)    |   156   |  4  |      **160**      |
| HC-L0-05 |   Zone F (Corridor, below R10)    |    10, 11     |   Zone E, F, D (Bottom)   |   164   |  6  |      **170**      | 
| HC-L0-06 | Zone C/G boundary (right of HC-03 |       6       | Zone C (Lef/Mid), G (Top) |   100   | 19  |      **119**      |
| HC-L0-07 |  Zone G (Middle Right of HC-04)   |       9       |         Zone G, C         |   64    |  5  |      **69**       |
| HC-L0-08 |  Zone G (Bottom Right of HC-05)   |       -       |         Zone J, I         |    0    |  4  |       **4**       |
| HC-L0-09 |   Zone H (Left of Middle Block)   |      14       |         Zone L, H         |   82    |  6  |      **88**       |
| HC-L0-10 |  Zone K (Right of Middle Block)   |      15       |         Zone J, I         |   80    |  6  |      **86**       |
| HC-L0-11 |      Zone L (Left Above R19)      |      19       |      Zone L (Bottom)      |   98    |  7  |      **105**      |
| HC-L0-12 |     Zone L (Right Above R20)      |      20       |       Zone L (Mid)        |   116   |  7  |      **123**      |
| HC-L0-13 |              Room 18              |       -       |     Room 16, 17*, 18      |    0    |  3  |      **121**      |
| HC-L0-14 |     Zone M (Between R21-R22)      |      21       |          Zone M           |   82    |  2  |      **84**       |
| HC-L0-15 |              Room 22              |       -       |          Room 22          |    0    |  1  |       **1**       |

*Note: Rooms 16 and 17 don't require outlets.*

* **Minimizing Distances:** The dispersion of 14 HCs (including 10 in the false ceiling of the open area) is the only way to 
guarantee that the hundreds of connections in the central zones of the terminal do not exceed the physical limit of the copper.

* **Access Point Management:** The HCs located in zones D, G, J, and L are dedicated almost exclusively to managing the 
density of Access Points, facilitating maintenance in the false ceiling.

* **Total HCs for Level 0: 15**

As each HC is positioned in the center of a **80.00 x 80.00 area**, the max distance of a piece of equipment to the HC 
will be the distance of the HC to the corner of the area. 

This distance is equal to **56.568$m$** which is well below the **80$m$** range of copper cables.

#### Schematic Plan (For APs and Dedicated Outlets)
> This schematic shows how to place the APs and their Dedicated Outlets.

![HCs Schematic](doc/sprint1/1241176/assets/Lvl0-Hc.svg)

---

#### 4.1.2. Level 2 (Departures)

|    HC    |         POSITION         | ROOMS COVERED |    AREAS COVERED    | OUTLETS | APs | TOTAL CONNECTIONS |
|:--------:|:------------------------:|:-------------:|:-------------------:|:-------:|:---:|:-----------------:|
| HC-L2-01 |          Room 1          |       3       |   Zone O (Top), A   |   52    |  4  |      **56**       |
| HC-L2-02 |          Room 2          |       -       |      Zone B, C      |    0    |  7  |       **7**       |
| HC-L2-03 |   Corridor (near R4-5)   |     4, 5      | Zone O (Upper-Mid)  |   116   |  4  |      **120**      |
| HC-L2-04 |     Zone F (near R7)     |     6, 7      |    Zone D, E, F     |   164   |  7  |      **171**      |
| HC-L2-05 |   Corridor (near R8-9)   |     8, 9      |    Zone O (Mid)     |   132   |  4  |      **136**      | 
| HC-L2-06 | Open Area (near G-H Top) |      10       |   Zone G, H (Top)   |   92    | 12  |      **104**      |
| HC-L2-07 |   Corridor (near R11)    |      11       | Zone O (Lower-Mid)  |   124   |  4  |      **128**      |
| HC-L2-08 |   Corridor (near R13)    |      13       | Zone O (Lower-Mid)  |   112   |  4  |      **116**      |
| HC-L2-09 |  Open Area (near H Mid)  |      12       |    Zone H (Mid)     |   100   |  8  |      **108**      |
| HC-L2-10 |  Corridor (near R14-15)  |    14, 15     |   Zone O (Lower)    |   168   |  5  |      **173**      |
| HC-L2-11 |  Zone I/J (near R16/17)  |      17       |      Zone I, J      |   82    |  5  |      **87**       |
| HC-L2-12 |  Corridor (near R14/15)  |      16       |      Zone M, K      |   86    |  6  |      **92**       |
| HC-L2-13 |    Zone M (near R24)     |       -       | Rooms 18-21, Zone L |    0    |  8  |       **8**       |
| HC-L2-14 |    Zone N (near R25)     |      24       | Zone H (Bottom), N  |   114   |  9  |      **123**      |
| HC-L2-15 |         Room 22          |      23       |   Zone O (Bottom)   |   98    |  3  |      **101**      |
| HC-L2-16 |         Room 26          |      25       |   Zone H (Corner)   |   82    |  3  |      **85**       |

> As there were two HCs that would surpass the limit of 200 connections, we had to divide it into 2 areas so we require 
two extra HC to cover the whole terminal.

*Note:The values marked with an asterisk accommodate the 110 exterior wall outlets required by the statement
(1 outlet every 5 meters), geographically distributed among the racks closest to the wall to avoid cables exceeding the 
90 m limit of the standard.*

As each HC is positioned in the center of a **80.00 x 80.00 area**, the max distance of a piece of equipment to the HC
will be the distance of the HC to the corner of the area.

This distance is equal to **56.568$m$** which is well below the **80$m$** range of copper cables.

**Total HCs for Level 2: 16 HCs**

#### Schematic Plan (For APs and Dedicated Outlets)
> This schematic shows how to place the APs and their Dedicated Outlets.

![HCs Schematic](doc/sprint1/1241176/assets/Lvl2-Hc.svg)

---

## 5. Cable Pathways

> The cable length is calculated by using a straight line between the HC and the room/area it serves.

> **MC → IC:** The MC will connect to the IC on both levels.

> **IC → HC:** The IC will connect to all HCs on its specific level, using the dropped ceiling.

> **Room Outlets:** $d_{HC \to room\_center} \times N_{outlets}$ — to simplify calculations

> **APs (room or open area):** $d_{HC \to AP\_position}$ – since each AP has a dedicated outlet

> **Cable Redundancy** will be considered to connect **MC → IC** and **IC → HC**

---

### 5.1. MC → IC (Backbone)

The Main Cross-Connect (MC) of the campus will connect to the Intermediate Cross-Connects (IC) of this building. 
We will position the ICs inside **Room 22** on both levels, as this room contains a vertical cable passageway that 
connects directly to the external underground technical ditch.

* **Level 0 (IC0):** The vertical distance between Level 0 and the external underground passageway is 3 meters.
* **Level 2 (IC2):** The vertical distance between Level 2 and the external underground passageway is 15 meters.
* **Internal Vertical Link (IC0 → IC2):** The physical vertical distance between IC0 (Level 0) and IC2 (Level 2) is 12 meters ($15m - 3m$).

These connections will be done with **Multimode Optical Fiber**.

* **Total internal vertical cable length (IC0 $\rightarrow$ IC2): 12$m$**
* **Total internal vertical cable length (with redundancy): 24$m$**

---

### 5.2. IC → HC

The IC of each level (located in Room 22) will connect directly to all HCs on its respective level using the dropped ceiling (4m height).

> These connections will be done with Multimode Optical Fiber since distances are below 500m.

---

#### 5.2.1. Level 0 (Arrivals)

|   CONNECTION   |        DISTANCE ($m$)        |
|:--------------:|:----------------------------:|
| IC0 → HC-L0-1  |       450 + 150 = 600        |
| IC0 → HC-L0-2  |             400              |
| IC0 → HC-L0-3  |    360 + 106.67 = 466.67     |
| IC0 → HC-L0-4  |    280 + 106.67 = 386.67     |
| IC0 → HC-L0-5  |    200 + 106.67 = 306.67     |
| IC0 → HC-L0-6  |        360 + 40 = 400        |
| IC0 → HC-L0-7  |       280 +  40 = 320        |
| IC0 → HC-L0-8  |        200 + 40 = 240        |
| IC0 → HC-L0-9  |    120 + 106.67 = 226.67     |
| IC0 → HC-L0-10 |        120 + 40 = 160        |
| IC0 → HC-L0-11 |     40 + 106.67 = 146.67     |
| IC0 → HC-L0-12 |         40 + 40 = 80         |
| IC0 → HC-L0-13 |             150              |
| IC0 → HC-L0-14 |            26.67             |
| IC0 → HC-L0-15 | 1 meter (located in room 22) |

**Total cable length for IC → HC connections: 3911.02 m**

**Total cable length for IC → HC connections (with cable redundancy): 7822.04 m**

---

#### 5.2.1. Level 2 (Departures)

|   CONNECTION   |         DISTANCE ($m$)          |
|:--------------:|:-------------------------------:|
| IC2 → HC-L2-1  |         400 + 150 = 600         |
| IC2 → HC-L2-2  |               400               |
| IC2 → HC-L2-3  |       375 + 112.5 = 487.5       |
| IC2 → HC-L2-4  |       375 + 37.5 = 412.5        |
| IC2 → HC-L2-5  |       287.5 + 112.5 = 400       |
| IC2 → HC-L2-6  |       287.5 + 37.5 = 325        |
| IC2 → HC-L2-7  |       212.5 + 112.5 = 325       |
| IC2 → HC-L2-8  |       162.5 + 87.5 = 250        |
| IC2 → HC-L2-9  |       212.5 + 37.5 = 253        |
| IC2 → HC-L2-10 |       125 + 112.5 = 237.5       |
| IC2 → HC-L2-11 |       125 + 37.5 = 162.5        |
| IC2 → HC-L2-12 |       50 + 112.5 = 162.5        |
| IC2 → HC-L2-13 |        50 + 37.5 = 87.5         |
| IC2 → HC-L2-14 |               25                |
| IC2 → HC-L2-15 |               150               |
| IC2 → HC-L2-16 | 1 meter (co-located in room 22) |

**Total cable length for IC → HC connections: 4279 m**

**Total cable length for IC → HC connections (with cable redundancy): 8558 m**

---

### 5.3. HC → Outlets

Each HC will connect to the outlets covered by its own area.

> These connections will be done with copper cables (Cat 6/6A U/FTP or S/FTP).

*\*We will use the formula previously mentioned for the calculations.*

---

#### 5.3.1. Level 0 (Arrivals)

To simplify the calculations of the outlets on the external walls, we will use the maximum distance between the HC 
and the corner of its covered area and multiply it by the number of external outlets covered for the HCs that cover part
of both external walls. For HCs that only cover part of one of the walls, we will use the distance between the HC 
and the middle of that part of the wall.

|    HC     | TOTAL LENGTH (m) |
|:---------:|:----------------:|
| HC-L0-01  |     3040.37      |
| HC-L0-02  |      173.33      | 
| HC-L0-03  |     3059.75      |
| HC-L0-04  |       450        |
| HC-L0-05  |      7467.2      |                  
| HC-L0-06  |      493.36      |
| HC-L0-07  |     6319.95      |
| HC-L0-08  |       420        |
| HC-L0-09  |      123.33      |
| HC-L0-10  |       6710       |
| HC-L0-11  |      256.68      |
| HC-L0-12  |       280        |
| HC-L0-13  |       3.33       |
| HC-L0-14  |     8847.33      |
| HC-L0-15  |       2000       |
| **Total** |       ****       |


![HCs Schematic](doc/sprint1/1241176/assets/LVL0-CABLE.svg)

---

#### 5.3.2. Level 2 (Departures)

|    HC     | TOTAL LENGTH (m) |
|:---------:|:----------------:|
| HC-L2-01  |     2615.629     |
| HC-L2-02  |      156.46      | 
| HC-L2-03  |                  |
| HC-L2-04  |                  |
| HC-L2-05  |                  |                  
| HC-L2-06  |                  |
| HC-L2-07  |                  |
| HC-L2-08  |                  |
| HC-L2-09  |                  |
| HC-L2-10  |                  |
| HC-L2-11  |                  |
| HC-L2-12  |                  |
| HC-L2-13  |                  |
| HC-L2-14  |                  |
| HC-L2-15  |                  |
| HC-L2-16  |                  |
| **Total** |       ****       |

![HCs Schematic](doc/sprint1/1241176/assets/lvl2-cable.svg)
---

## 6. Hardware Inventory

### 6.1. End-User and Wireless Equipment

This section details the physical interfaces and devices deployed across the work areas and false ceilings to provide wired and wireless LAN access.

| EQUIPMENT | LEVEL 0 (ARRIVALS) | LEVEL 2 (DEPARTURES) | TOTAL |
| :--- | :---: | :---: | :---: |
| **Standard Network Outlets (ISO 8877)** | 1192 | 1522 | **2714** |
| **Dedicated Outlets (for APs)** | 88 | 93 | **181** |
| **Wireless Access Points (APs)** | 88 | 93 | **181** |

---

### 6.2. Telecommunications Enclosures and Terminations

This section details the hardware required to accommodate the cross-connections.
*Note: The number of 24-port Patch Panels was calculated individually for each Horizontal Cross-Connect (HC) by dividing its specific total connections by 24 and rounding up, ensuring accurate physical distribution.*

| EQUIPMENT | LEVEL 0 (ARRIVALS) | LEVEL 2 (DEPARTURES) | TOTAL |
| :--- | :---: | :---: | :---: |
| **Horizontal Cross-Connects (HCs)** | 15 | 16 | **31** |
| **Intermediate Cross-Connects (ICs)** | 1 | 1 | **2** |
| **Enclosures / Racks (42U)** | 15 | 16 | **31** |
| **Total Copper Connections (Cables)** | 1280 | 1615 | **2895** |
| **24-Port Patch Panels** | 61 | 76 | **137** |

> **Enclosure Usage Justification:** The 31 assigned 42U enclosures provide abundant space for the required hardware. 
> Even the most heavily loaded HC (HC-L2-10 with 173 connections) only requires 8 patch panels (8U). 
> This leaves more than 30U of free space in every rack for the active equipment (Switches, PoE injectors), 
fiber optic patch panels, cable management organizers, and future network expansions.