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

|    HC    | ROOMS COVERED  |        AREAS COVERED        | OUTLETS  | APs | TOTAL CONNECTIONS |
|:--------:|:--------------:|:---------------------------:|:--------:|:---:|:-----------------:|
| HC-L0-01 |      1, 3      |              A              | 112 + 3  |  3  |      **118**      |
| HC-L0-02 |       -        |              B              |    4     |  4  |       **8**       |
| HC-L0-03 |      4, 5      |           D (Top)           | 138 + 4  |  4  |      **146**      |
| HC-L0-04 |       -        |           C (Top)           |    10    | 10  |      **20**       |
| HC-L0-05 |      6, 7      |         D (Middle)          | 156 + 6  |  6  |      **168**      |
| HC-L0-06 |      8, 9      |         C (Bottom)          | 164 + 10 | 10  |      **184**      |
| HC-L0-07 | 10, 11, 12, 13 |    D (Mid-Bottom), E, F     | 164 + 8  |  8  |      **180**      |
| HC-L0-08 |       -        |              G              |    10    | 10  |      **20**       |
| HC-L0-09 |       -        |     D (Lower-Bottom), H     |    4     |  4  |       **8**       |
| HC-L0-10 |     14, 15     |           J, I, K           | 160 + 6  |  6  |      **172**      |
| HC-L0-11 |       17       | D (Bottom), L (Left Corner) |    4     |  4  |       **8**       |
| HC-L0-12 |       -        |              L              |    10    | 10  |      **20**       |
| HC-L0-13 |   16, 18, 19   |              -              |  98 + 3  |  3  |      **104**      |
| HC-L0-14 |       20       |              M              | 116 + 3  |  3  |      **122**      |
| HC-L0-15 |     21, 22     |              -              |  82 + 1  |  1  |      **84**       |


* **Minimizing Distances:** The dispersion of 15 HCs (including 10 in the false ceiling of the open area) is the only way to
  guarantee that the hundreds of connections in the central zones of the terminal do not exceed the physical limit of the copper.

* **Access Point Management:** The HCs located in zones D, G, J, and L are dedicated almost exclusively to managing the
  density of Access Points, facilitating maintenance in the false ceiling.

* **Total HCs for Level 0: 15**

As each HC is positioned in the center of a **80.00 x 80.00 area**, the max distance of an equipment piece to the HC
will be the distance of the HC to the corner of the area.

This distance is equal to **56.568$m$** which is well below the **80$m$** range of copper cables.

#### Schematic Plan (For APs and Dedicated Outlets)
> This schematic shows how to place the Horizontal Cross-connect.

![HCs Schematic](doc/sprint2/1241176/assets/Terminal5_Lvl0_HCs.svg)

---

#### 4.1.2. Level 2 (Departures)

|    HC    | ROOMS COVERED |           AREAS COVERED           | OUTLETS | APs | TOTAL CONNECTIONS |
|:--------:|:-------------:|:---------------------------------:|:-------:|:---:|:-----------------:|
| HC-L2-01 |       3       |          Zone O (Top), A          |   52    |  4  |      **56**       |
| HC-L2-02 |       -       |              Zone B               |    0    |  4  |       **4**       |
| HC-L2-03 |     4, 5      |       Zone O (Upper-Mid), C       |   116   |  5  |      **121**      |
| HC-L2-04 |     6, 7      |           Zone D, E, F            |   164   |  6  |      **170**      |
| HC-L2-05 |     8, 9      |     Zone G (Top), O (Middle)      |   132   |  5  |      **137**      | 
| HC-L2-06 |      10       |           Zone H (Top)            |   92    | 11  |      **103**      |
| HC-L2-07 |      12       | Zone O (Lower-Mid), G (Lower-Mid) |   100   |  6  |      **106**      |
| HC-L2-08 |      11       |           Zone H (Mid)            |   124   | 11  |      **135**      |
| HC-L2-09 |      13       |  Zone G (Bottom), O (Lower-Mid)   |   112   |  3  |      **116**      |
| HC-L2-10 |    14, 15     |     Zone O (Lower), G (Lower)     |   168   |  6  |      **174**      |
| HC-L2-11 |      17       |          Zone H (Lower)           |   82    |  5  |      **87**       |
| HC-L2-12 |      16       |           Zone L, K, I            |   86    |  6  |      **92**       |
| HC-L2-13 |       -       |             Zone J, M             |    0    |  8  |       **8**       |
| HC-L2-14 |  18, 19, 23   |                 -                 |   98    |  4  |      **102**      |
| HC-L2-15 |    24, 25     |              Zone N               |   196   |  2  |      **198**      |
| HC-L2-16 |      26       |                 -                 |    0    |  2  |       **2**       |

> As there were two HCs that would surpass the limit of 200 connections, we had to divide it into 2 areas so we require
two extra HC to cover the whole terminal.

As each HC is positioned in the center of a **80.00 x 80.00 area**, the max distance of a piece of equipment to the HC
will be the distance of the HC to the corner of the area.

This distance is equal to **56.568$m$** which is well below the **80$m$** range of copper cables.

**Total HCs for Level 2: 16 HCs**

#### Schematic Plan (For APs and Dedicated Outlets)
> This schematic shows how to place the Horizontal Cross-connect.

![HCs Schematic](doc/sprint2/1241176/assets/Terminal5_Lvl2_HCs.svg)

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
We will position the ICs inside **Room 22** on **Level 0** and **Room 26** on **Level 2**, as this room contains a
vertical cable passageway that connects directly to the external underground technical ditch.

* **Level 0 (IC0):** The vertical distance between Level 0 and the external underground passageway is 3 meters.
* **Level 2 (IC2):** The vertical distance between Level 2 and the external underground passageway is 15 meters.
* **Internal Vertical Link (IC0 → IC2):** The physical vertical distance between IC0 (Level 0) and IC2 (Level 2) is 12 meters ($15m - 3m$).

These connections will be done with **Multimode Optical Fiber**.

* **Total internal vertical cable length (IC0 $\rightarrow$ IC2): 12$m$**
* **Total internal vertical cable length (with redundancy): 24$m$**

---

### 5.2. IC → HC

The IC of each level (located in Rooms 22 and 26) will connect directly to all HCs on its respective level using the
dropped ceiling (4m height).

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
| IC0 → HC-L0-14 |            76.67             |
| IC0 → HC-L0-15 | 1 meter (located in room 22) |

**Total cable length for IC → HC connections: 3961.02 m**

**Total cable length for IC → HC connections (with cable redundancy): 7922.04 m**

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

| **HC**             | **TYPE**                                                                                                   | **CABLES** | **TOTAL CABLE LENGTH** |
|:-------------------|:-----------------------------------------------------------------------------------------------------------|:----------:|:----------------------:|
| HC-L0-1            | APs — 3 cables (3.33m, 23.33m, 26.67m)                                                                     |     3      |         53.33m         |
| HC-L0-1            | Room outlets (R3: 26.67m × 112)                                                                            |    112     |        2986.67m        |
| **HC-L0-1 Total**  | -                                                                                                          |  **115**   |       **3040m**        |
| HC-L0-2            | APs — 4 cables (3.33m, 23.33m, 50m, 76.67m)                                                                |     4      |        153.33m         |
| **HC-L0-2 Total**  | -                                                                                                          |   **4**    |      **153.33m**       |
| HC-L0-3            | APs — 4 cables (30m, 56.67m, 10m, 26.67m)                                                                  |     4      |        123.34m         |
| HC-L0-3            | Room outlets (R4: 10m × 74)                                                                                |     74     |          740m          |
| HC-L0-3            | Room outlets (R5: 26.67m × 64)                                                                             |     64     |        1706.67m        |
| **HC-L0-3 Total**  | -                                                                                                          |  **142**   |      **2356.67m**      |
| HC-L0-4            | APs — 10 cables (20m, 10m, 36.67m, 26.67m, 53.33m, 46.67m, 76.67m, 66.67m, 50m, 96.67m)                    |     10     |        483.34m         |
| **HC-L0-4 Total**  | -                                                                                                          |   **10**   |      **483.34m**       |
| HC-L0-5            | Room outlets (R6: 43.33m × 100)                                                                            |    100     |        4333.33m        |
| HC-L0-5            | Room outlets (R7: 16.67m × 56)                                                                             |     56     |        933.33m         |
| HC-L0-5            | APs — 2 cables (30m, 53.33m)                                                                               |     2      |         83.33m         |
| **HC-L0-5 Total**  | -                                                                                                          |  **158**   |      **5349.99m**      |
| HC-L0-6            | Room outlets (R8: 96.67m × 100)                                                                            |    100     |        9666.67m        |
| HC-L0-6            | Room outlets (R9: 120m × 64)                                                                               |     64     |         7680m          |
| HC-L0-6            | APs — 10 cables (23.33m, 26.67m, 46.67m, 66.67m, 53.33m, 36.67m, 60m, 80m, 103.33m, 3.33m)                 |     10     |          500m          |
| **HC-L0-6 Total**  | -                                                                                                          |  **174**   |     **17846.67m**      |
| HC-L0-7            | Room outlets (R10: 20m × 88)                                                                               |     88     |         1760m          |
| HC-L0-7            | Room outlets (R11: 16.67m × 76)                                                                            |     76     |        1266.67m        |
| HC-L0-7            | APs — 6 cables (30m, 3.33m, 16.67m, 33.33m, 46.67m, 43.33m)                                                |     6      |        173.33m         |
| **HC-L0-7 Total**  | -                                                                                                          |  **170**   |       **3200m**        |
| HC-L0-8            | APs — 10 cables (23.33m, 13.33m, 26.67m, 46.67m, 63.33m, 43.33m, 30m, 46.67m, 63.33m, 83.33m)              |     10     |        439.99m         |
| **HC-L0-8 Total**  | -                                                                                                          |   **10**   |      **439.99m**       |
| HC-L0-9            | APs — 4 cables (20m, 20m, 40m, 43.33m)                                                                     |     4      |        123.33m         |
| **HC-L0-9 Total**  | -                                                                                                          |   **4**    |      **123.33m**       |
| HC-L0-10           | Room outlets (R14: 56.67m × 83)                                                                            |     83     |        4703.33m        |
| HC-L0-10           | Room outlets (R15: 30m × 80)                                                                               |     80     |         2430m          |
| HC-L0-10           | APs — 4 cables (40m, 26.67m, 20m, 23.33m)                                                                  |     4      |          110m          |
| **HC-L0-10 Total** | -                                                                                                          |  **167**   |      **7243.33m**      |
| HC-L0-11           | APs — 4 cables (30m, 40m, 3.33m, 26.67m)                                                                   |     4      |         99.99m         |
| **HC-L0-11 Total** | -                                                                                                          |   **4**    |       **99.99m**       |
| HC-L0-12           | APs — 10 cables (30m, 10m, 30m, 50m, 66.67m, 83.33m, 66.67m, 46.67m, 36.67m, 50m)                          |     10     |          470m          |
| **HC-L0-12 Total** | -                                                                                                          |   **10**   |        **470m**        |
| HC-L0-13           | APs — 2 cables (13.33m, 3.33m)                                                                             |     2      |         16.67m         |
| HC-L0-13           | Room outlets (R19: 20m × 98)                                                                               |     98     |         1980m          |
| **HC-L0-13 Total** | -                                                                                                          |  **100**   |      **1996.67m**      |
| HC-L0-14           | Room outlets (R20: 23.33m × 116)                                                                           |    116     |        2706.67m        |
| **HC-L0-14 Total** | -                                                                                                          |  **116**   |      **2706.67m**      |
| HC-L0-15           | APs — 2 cables (3.33m, 10m)                                                                                |     2      |         13.33m         |
| HC-L0-15           | Room outlets (R21: 40m × 82)                                                                               |     82     |         3280m          |
| **HC-L0-15 Total** | -                                                                                                          |   **84**   |      **3293.33m**      |
| **Level 0 Total**  | -                                                                                                          |  **1068**  |     **48803.31m**      |


![Level 0 Cable Schematic](doc/sprint2/1241176/assets/Terminal5_Lvl0_Cables.svg)

---

#### 5.3.2. Level 2 (Departures)

| **HC**             | **TYPE**                                                                                                  | **CABLES**  | **TOTAL CABLE LENGTH**  |
|:-------------------|:----------------------------------------------------------------------------------------------------------|:-----------:|:-----------------------:|
| HC-L2-1            | Room outlets (R3: 37.5m * 52)                                                                             |     52      |          1950m          |
| HC-L2-1            | APs — 3 cables (31.25m, 21.875m, 3.125m)                                                                  |      3      |         56.25m          |
| **HC-L2-1 Total**  | -                                                                                                         |   **55**    |      **2006.25m**       |
| HC-L2-2            | APs — 4 cables (25m, 50m, 75m, 3.125m)                                                                    |      4      |        153.125m         |
| **HC-L2-2 Total**  | -                                                                                                         |    **4**    |      **153.125m**       |
| HC-L2-3            | Room outlets (R14: 3.125m * 52, R15: 21.875m * 64)                                                        |     116     |         1562.5m         |
| HC-L2-3            | APs — 3 cables (56.25m, 31.25m, 31.25m)                                                                   |      3      |         118.75m         |
| **HC-L2-3 Total**  | -                                                                                                         |   **119**   |      **1681.25m**       |
| HC-L2-4            | Room outlets (R7: 12.5m * 82, R6: 43.75m * 82)                                                            |     164     |         4612.5m         |
| HC-L2-4            | APs — 4 cables (18.75m, 18.75m, 15.625m, 34.375m)                                                         |      4      |          87.5m          |
| **HC-L2-4 Total**  | -                                                                                                         |   **168**   |        **4700m**        |
| HC-L2-5            | Room outlets (R9: 18.75m * 44, R8: 40.625m * 88)                                                          |     132     |          4400m          |
| HC-L2-5            | APs — 3 cables (21.875m, 50m, 37.5m)                                                                      |      3      |        109.375m         |
| **HC-L2-5 Total**  | -                                                                                                         |   **135**   |      **4509.375m**      |
| HC-L2-6            | Room outlets (R10: 103.125m * 92)                                                                         |     92      |         9487.5m         |
| HC-L2-6            | APs — 10 cables (12.5m, 28.125m, 15.625m, 43.75m, 40.625m, 43.75m, 56.25m, 68.75m, 40.625m, 56.25m)       |     10      |         406.25m         |
| **HC-L2-6 Total**  | -                                                                                                         |   **102**   |      **9893.75m**       |
| HC-L2-7            | Room outlets (R12: 21.875m * 100)                                                                         |     100     |         2187.5m         |
| HC-L2-7            | APs — 5 cables (84.375m, 34.375m, 71.875m, 25m, 43.75m)                                                   |      5      |        259.375m         |
| **HC-L2-7 Total**  | -                                                                                                         |   **105**   |      **2446.875m**      |
| HC-L2-8            | Room outlets (R11: 103.125m * 124)                                                                        |     124     |        12787.5m         |
| HC-L2-8            | APs — 10 cables (53.125m, 62.5m, 46.875m, 37.5m, 25m, 31.25m, 21.875m, 40.625m, 46.875m, 34.375m)         |     10      |          400m           |
| **HC-L2-8 Total**  | -                                                                                                         |   **134**   |      **13187.5m**       |
| HC-L2-9            | Room outlets (R13: 18.75m * 112)                                                                          |     112     |          2100m          |
| HC-L2-9            | APs — 2 cables (9.375m, 46.875m)                                                                          |      2      |         56.25m          |
| **HC-L2-9 Total**  | -                                                                                                         |   **114**   |      **2156.25m**       |
| HC-L2-10           | Room outlets (R14: 21.875m * 60, R15: 21.875m * 108)                                                      |     168     |          3675m          |
| HC-L2-10           | APs — 4 cables (40.625m, 25m, 59.375m, 87.5m)                                                             |      4      |         212.5m          |
| **HC-L2-10 Total** | -                                                                                                         |   **172**   |       **3887.5m**       |
| HC-L2-11           | APs — 10 cables (40.625m, 34.375m, 25m, 18.75m, 31.25m, 25m, 43.75m, 40.625m, 56.25m, 50m)                |     10      |        365.625m         |
| **HC-L2-11 Total** | -                                                                                                         |   **10**    |      **365.625m**       |
| HC-L2-12           | APs — 6 cables (15.625m, 31.25m, 12.5m, 25m, 53.125m, 59.375m)                                            |      6      |        196.875m         |
| **HC-L2-12 Total** | -                                                                                                         |    **6**    |      **196.875m**       |
| HC-L2-13           | Room outlets (R17: 34.375m * 82, R16: 53.125m * 86)                                                       |     168     |         7387.5m         |
| HC-L2-13           | APs — 5 cables (21.875m, 34.375m, 12.5m, 34.375m, 56.25m)                                                 |      5      |        159.375m         |
| **HC-L2-13 Total** | -                                                                                                         |   **173**   |      **7546.875m**      |
| HC-L2-14           | Room outlets (R23: 15.625m * 98)                                                                          |     98      |        1531.25m         |
| HC-L2-14           | APs — 3 cables (15.625m, 25m, 3.125m)                                                                     |      3      |         43.75m          |
| **HC-L2-14 Total** | -                                                                                                         |   **101**   |        **1575m**        |
| HC-L2-15           | APs — 2 cables (18.75m, 50m)                                                                              |      2      |         68.75m          |
| **HC-L2-15 Total** | -                                                                                                         |    **2**    |       **68.75m**        |
| HC-L2-16           | APs — 2 cables (3.125m, 15.625m)                                                                          |      2      |         18.75m          |
| **HC-L2-16 Total** | -                                                                                                         |    **2**    |       **18.75m**        |
| **Level 2 Total**  | -                                                                                                         |  **1402**   |      **54112.5m**       |


![Level 2 Cable Schematic](doc/sprint2/1241176/assets/Terminal5_Lvl2_Cables.svg)

---

## 6.Hardware Inventory

This section details the physical interfaces and devices deployed across the work areas and false ceilings to provide wired and wireless LAN access.


| Item                                        |  Level 0  | Level 2  |   **Total**    |
|:--------------------------------------------|:---------:|:--------:|:--------------:|
| Main Cross-connect (MC)                     |     -     |    —     |       -        |
| Intermediate Cross-connects (IC)            |     1     |    1     |     **2**      |
| Horizontal Cross-connects (HC)              |    15     |    16    |     **31**     |
| Access Points (Wi-Fi 5GHz)                  |    88     |    93    |    **181**     |
| Standard Oultlets                           |   1192    |   1522   |    **2714**    |
| Dedicated Outlets                           |    88     |    93    |    **181**     |
| Copper cable CAT7 (Horizontal)              | 48803.31m | 54112.5m | **102915.81m** |
| Multimode Optical Fibre (MC → IC + IC → HC) | 7922.04m  |  8558m   | **16504.04m**  |

*Note: The number of 24-port Patch Panels was calculated individually for each Horizontal Cross-Connect (HC) by dividing
its specific total connections by 24 and rounding up, ensuring accurate physical distribution.*

> **Enclosure Usage Justification:** The 31 assigned 42U enclosures provide abundant space for the required hardware.
> Even the most heavily loaded HC (HC-L2-10 with 173 connections) only requires 8 patch panels (8U).
> This leaves more than 30U of free space in every rack for the active equipment (Switches, PoE injectors),
fiber optic patch panels, cable management organizers, and future network expansions.