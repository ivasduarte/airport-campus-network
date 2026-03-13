# Terminal 3

---

## 0. Terminal Information

Has five floors.

Project only encompasses the first and second floor.

Wireless LAN coverage required (Wi-Fi).

---

## 1. Level 1 Information

Underfloor cable raceway with access points.

Four vertical cable passageways traveling across all floors of the building.

At a lower floor, these passageways have a direct connection to the external underground passageway.

Vertical distance between this floor and the connection to the external underground passageway is 10m.

Ceiling height is 5m.

Dropped ceiling placed 4m above ground.

Space above dropped ceiling is perfect to install cable raceways and wireless access points.

Rooms 1, 11 and 15 are suitable for housing network infrastructure hardware.

---

## 2. Level 2 Information

Underfloor cable raceway with access points.

Four vertical cable passageways traveling across all the floors of the building.

At a lower floor, these passageways have a direct external connection to the external underground passageway.

Vertical distance between this floor and the connection to the external underground passageway is 16m.

Ceiling height is 5m.

Dropped ceiling placed 4m above ground.

Space above dropped ceiling is perfect to install cable raceways and wireless access points.

Rooms 1, 13 and 20 are suitable for housing network infrastructure hardware.

---

## 3. Scale & Measurements

The measurements will be done utilizing pixels and then converted to meters.

* **Building dimensions:** 200$m$ × 200$m$ = 40000$m^2$;
* **Scale Used:** 577$px$ = 200$m$ → 1$px$ = 0.3466$m$;

**Formula to convert pixels to meters** → `(x * 200)/577 = y`
> x = value in pixels, y = value in meters

---

## 4. Network Outlets Calculation

**Standard rule:** 2 outlets per every 10$m^2$ → `working_areas = area / 10` → `outlets = working_areas × 2`
> When calculating working areas, the result will always be rounded **up** to ensure full area coverage.

---

### 4.1 Level 1 (Arrivals)

> Rooms 2, 4, 5, 7, 8, 9, 10, 12, 13 and 14 are to be provided with the standard number of network outlets (2 per 10m²).
>
> Rooms 1, 3, 6, 11 and 15 are not required to have network outlets.

| Rooms | Dimensions (px) | Dimensions (m) | Area (m^2) | Working Areas | Outlets |
|-------|-----------------|----------------|------------|---------------|---------|
| 1     | 21x38           | 7.28x13.17     | 95.88      | --            | --      |
| 2     | 37x53           | 12.82x18.37    | 235.61     | 24            | 48      |
| 3     | 45x69           | 15.60x23.92    | 373.05     | --            | --      |
| 4     | 37x53           | 12.82x18.37    | 235.61     | 24            | 48      |
| 5     | 55x37           | 19.06x12.82    | 244.50     | 25            | 50      |
| 6     | 45x68           | 15.60x23.57    | 367.55     | --            | --      |
| 7     | 37x53           | 12.82x18.37    | 235.61     | 24            | 48      |
| 8     | 37x37           | 12.82x12.82    | 164.48     | 17            | 34      |
| 9     | 37x45           | 12.82x15.60    | 200.04     | 21            | 42      |
| 10    | 37x68           | 12.82x23.57    | 302.29     | 31            | 62      |
| 11    | 28x28           | 9.71x9.71      | 94.19      | --            | --      |
| 12    | 37x83           | 12.82x28.77    | 368.97     | 37            | 74      |
| 13    | 92x36           | 31.89x12.48    | 397.92     | 40            | 80      |
| 14    | 61x36           | 21.14x12.48    | 263.84     | 27            | 54      |
| 15    | 29x36           | 10.05x12.48    | 125.43     | --            | --      |

> One network outlet (ISO 8877) is required every 5m along the external wall on the left side of the plan and along the external wall at the upper side of the plan.

| Wall | Length ($m$) | Outlets |
|------|--------------|---------|
| Left | 200          | **40**  |
| Top  | 200          | **40**  |

As the walls form a 90º angle with each other, they have a common outlet so, in total, we'll have 79 outlets along the external walls.

**Total standard outlets for Level 1: 540 (Rooms) + 79 (External walls) = 619**

---

### 4.2 Level 2 (Departures)

> Rooms 2, 3, 4, 7, 10, 11, 12, 14, 15, 16, 17, 18 and 19 are to be provided with the standard number of network outlets (2 per 10m²).
> 
> Rooms 1, 5, 6, 8, 9, 13 and 20 are not required to have network outlets.

| Rooms | Dimensions (px) | Dimensions (m) | Area (m^2) | Working Areas | Outlets |
|-------|-----------------|----------------|------------|---------------|---------|
| 1     | 21x38           | 7.28x13.17     | 95.88      | --            | --      |
| 2     | 36x67           | 12.48x23.22    | 289.79     | 29            | 58      |
| 3     | 119x36          | 41.25x12.48    | 514.70     | 52            | 104     |
| 4     | 36x67           | 12.48x23.22    | 289.79     | 29            | 58      |
| 5     | 43x60           | 14.90x20.80    | 309.98     | --            | --      |
| 6     | 44x68           | 15.25x23.57    | 359.48     | --            | --      |
| 7     | 78x35           | 27.04x12.13    | 328.00     | 33            | 66      |
| 8     | 42x59           | 14.56x20.45    | 297.72     | --            | --      |
| 9     | 44x68           | 15.25x23.57    | 359.48     | --            | --      |
| 10    | 123x36          | 42.63x12.48    | 532.01     | 54            | 108     |
| 11    | 42x60           | 14.56x20.80    | 302.77     | 31            | 62      |
| 12    | 42x53           | 14.56x18.37    | 267.44     | 27            | 54      |
| 13    | 28x28           | 9.71x9.71      | 94.19      | --            | --      |
| 14    | 93x36           | 32.24x12.48    | 402.25     | 41            | 82      |
| 15    | 109x36          | 37.78x12.48    | 471.45     | 48            | 86      |
| 16    | 75x36           | 26.00x12.48    | 324.39     | 33            | 66      |
| 17    | 63x36           | 21.84x12.48    | 272.49     | 28            | 56      |
| 18    | 93x36           | 32.24x12.48    | 402.25     | 41            | 62      |
| 19    | 61x36           | 21.14x12.48    | 263.84     | 37            | 74      |
| 20    | 29x36           | 10.05x12.48    | 125.43     | --            | --      |

**Total standard outlets for Level 2: 936**

---

## 5. Access Points Calculations

> Both floors require full LAN coverage.
>
> Each Access Point covers a circular area with 50$m$ of diameter.
>
> All Access Points will be installed in the area between the dropped ceiling and the real ceiling
>
> Each Access Point will require **a dedicated outlet**
>
> All Access Points on this terminal will operate on **5GHz band**, since this band offers a larger number of available channels. Moreover, it also has **DFS (Dynamic Frequency Selection)**, which selects a channel in order avoid interference with its neighbours.

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

### 5.1. Level 1 (Arrivals)

First we calculate the number of access points required in each of the rooms of Level 1. We do this verification with the condition mentioned before ($D_a \leq D_c$). If the condition is verified to be true, we only require 1 access point, if not, we have to calculate $n$ to obtain the amount required.

| Rooms | $D_a$ (Diagonal) | Number of Acccess Points | Position ($m$) |
|-------|------------------|--------------------------|----------------|
| 1     | 15.05            | 1                        | 3.64x6.585     |
| 2     | 22.40            | 1                        | 6.41x9.185     |
| 3     | 28.56            | 1                        | 7.80x11.96     |
| 4     | 22.40            | 1                        | 6.41x9.185     |
| 5     | 22.97            | 1                        | 9.53x6.41      |
| 6     | 28.26            | 1                        | 7.80x11.785    |
| 7     | 22.40            | 1                        | 6.41x9.185     |
| 8     | 18.13            | 1                        | 6.41x6.41      |
| 9     | 20.19            | 1                        | 6.41x7.80      |
| 10    | 26.83            | 1                        | 6.41x11.785    |
| 11    | 13.73            | 1                        | 4.855x4.855    |
| 12    | 31.49            | 1                        | 6.41x14.385    |
| 13    | 34.24            | 1                        | 15.945x6.24    |
| 14    | 24.55            | 1                        | 10.57x6.24     |
| 15    | 16.02            | 1                        | 5.025x6.24     |

Now we divide the remaining open areas in rectangles and do the same verification that was used previously for the rooms of the level.
The open areas will be identified with letters in the schematic plan.

| Open Areas | Dimensions ($px$) | Dimensions ($m$) | Area ($m²$) | $D_a$ (Diagonal) | Number of Lines | Number of Access Points |
|------------|-------------------|------------------|-------------|------------------|-----------------|-------------------------|
| A          | 573x92            | 198.61x31.89     | 6333.67     | 201.15           | 1               | 7                       |
| B          | 277x174           | 96.01x60.31      | 5790.36     | 113.38           | 2               | 8                       |
| C          | 68x28             | 23.57x9.71       | 228.86      | 25.49            | 1               | 1                       |
| D          | 206x125           | 71.40x43.33      | 3093.762    | 83.52            | 1               | 4                       |
| E          | 364x65            | 126.17x22.53     | 2842.61     | 128.17           | 1               | 4                       |
| F          | 237x172           | 82.15x59.62      | 4897.78     | 101.50           | 2               | 8                       |
| G          | 205x68            | 71.06x23.57      | 1674.88     | 74.87            | 1               | 3                       |
| H          | 85x41             | 29.46x14.21      | 418.63      | 32.71            | 1               | 1                       |
| I          | 59x41             | 20.45x14.21      | 290.60      | 24.90            | 1               | 1                       |
| J          | 205x90            | 71.06x31.20      | 2217.07     | 77.61            | 1               | 3                       |
| K          | 47x60             | 16.29x20.80      | 338.83      | 26.42            | 1               | 1                       |
| L          | 293x162           | 101.56x56.15     | 5702.59     | 116.05           | 2               | 8                       |
| M          | 101x38            | 35.01x13.17      | 461.08      | 37.41            | 1               | 1                       |

**Open Area A**
- $n_{lines} = 1$
- $y = 15.945 m$
- $d = 15.945 m$
- $c = 19.255 m$
- $n_{APs} = 7$
- $spacing = 26.68 m$

| Access Point | Position ($m$) |
|--------------|----------------|
| 1            | 19.255x15.945  |
| 2            | 45.935x15.945  |
| 3            | 72.615x15.945  |
| 4            | 99.295x15.945  |
| 5            | 125.975x15.945 |
| 6            | 152.655x15.945 |
| 7            | 179.335x15.945 |

**Open Area B**
- $n_{lines} = 2$
- $y_1 = 15.078 m$
- $d_1 = 15.078 m$
- $c_1 = 19.94 m$
- $n_{APs1} = 4$
- $y_2 = 45.232 m$
- $d_2 = 15.078 m$
- $c_2 = 19.94m$
- $n_{APs2} = 4$
- $spacing = 18.71 m$

| Access Point | Position ($m$) |
|--------------|----------------|
| 1            | 19.94x15.078   |
| 2            | 38.65x15.078   |
| 3            | 57.36x15.078   |
| 4            | 76.07x15.078   |
| 5 _          | 19.94x45.232   |
| 6            | 38.65x45.232   |
| 7            | 57.36x45.232   |
| 8            | 76.07x45.232   |

**Open Area D**
- $n_{lines} = 1$
- $y = 21.665 m$
- $d = 21.665 m$
- $c = 12.48 m$
- $n_{APs} = 4$
- $spacing = 15.48 m$

| Access Point | Position ($m$) |
|--------------|----------------|
| 1            | 12.48x21.665   |
| 2            | 27.96x21.665   |
| 3            | 43.44x21.665   |
| 4            | 58.92x21.665   |

**Open Area E**
- $n_{lines} = 1$
- $y = 11.265 m$
- $d = 11.265 m$
- $c = 22.32 m$
- $n_{APs} = 4$
- $spacing = 27.18 m$

| Access Point | Position ($m$) |
|--------------|----------------|
| 1            | 22.32x11.265   |
| 2            | 49.50x11.265   |
| 3            | 76.68x11.265   |
| 4            | 103.86x11.265  |

**Open Area F**

- $n_{lines} = 2$
- $y_1 = 14.91 m$
- $d_1 = 14.91 m$
- $c_1 = 20.067 m$
- $n_{APs1} = 4$
- $spacing_1 = 14.01 m$
- $y_2 = 44.715 m$
- $d_2 = 15.445 m$
- $c_2 = 19.66 m$
- $n_{APs2} = 4
- $spacing_2 = 14.28 m$

| Access Point | Position ($m$) |
|--------------|----------------|
| 1            | 20.067x14.91   |
| 2            | 34.077x14.91   |
| 3            | 48.087x14.91   |
| 4            | 62.097x14.91   |
| 5            | 19.66x44.715   |
| 6            | 33.94x44.715   |
| 7            | 48.22x44.715   |
| 8            | 62.50x44.715   |

**Open Area G**
- $n_{lines} = 1$
- $y = 11.785 m$
- $d = 11.785 m$
- $c = 22.048 m$
- $n_{APs} = 3$
- $spacing = 13.482 m$

| Access Point | Position ($m$) |
|--------------|----------------|
| 1            | 22.048x11.785  |
| 2            | 35.53x11.785   |
| 3            | 49.012x11.785  |

**Open Area J**
- $n_{lines} = 1$
- $y = 15.60 m$
- $d = 15.60 m$
- $c = 19.54 m$
- $n_{APs} = 3$
- $spacing = 15.99 m$

| Access Point | Position ($m$) |
|--------------|----------------|
| 1            | 19.54x15.60    |
| 2            | 35.53x15.60    |
| 3            | 51.52x15.60    |

**Open Area L**
- $n_{lines} = 2$
- $y_1 = 14.04 m$
- $d_1 = 14.04 m$
- $y_2 = 42.11 m$
- $d_2 = 14.04 m$
- $c = 20.69 m$
- $n_{APs} = 4$
- $spacing = 20.06 m$

| Access Point | Position ($m$) |
|--------------|----------------|
| 1            | 20.69x14.04    |
| 2            | 40.75x14.04    |
| 3            | 60.81x14.04    |
| 4            | 80.87x14.04    |
| 5            | 20.69x42.11    |
| 6            | 40.75x42.11    |
| 7            | 60.81x42.11    |
| 8            | 80.87x42.11    |

---

### 5.2. Level 2 (Departures)

| Rooms | $D_a$ (Diagonal) | Number of Acccess Points | Position ($m$) |
|-------|------------------|--------------------------|----------------|
| 1     | 15.05            | 1                        | 3.64x6.585     |
| 2     | 22.40            | 1                        | 6.24x11.61     |
| 3     | 43.10            | 1                        | 20.625x6.24    |
| 4     | 26.36            | 1                        | 6.24x11.61     |
| 5     | 25.59            | 1                        | 7.45x10.40     |
| 6     | 28.07            | 1                        | 7.625x11.785   |
| 7     | 29.64            | 1                        | 13.52x6.065    |
| 8     | 25.10            | 1                        | 7.28x10.255    |
| 9     | 28.07            | 1                        | 7.625x11.785   |
| 10    | 44.42            | 1                        | 21.315x6.24    |
| 11    | 25.39            | 1                        | 7.28x10.40     |
| 12    | 23.44            | 1                        | 7.28x9.185     |
| 13    | 13.73            | 1                        | 4.855x4.855    |
| 14    | 34.57            | 1                        | 16.12x6.24     |
| 15    | 39.79            | 1                        | 18.89x6.24     |
| 16    | 28.84            | 1                        | 13.00x6.24     |
| 17    | 25.15            | 1                        | 10.92x6.24     |
| 18    | 34.57            | 1                        | 16.12x6.24     |
| 19    | 24.55            | 1                        | 10.57x6.24     |
| 20    | 16.02            | 1                        | 5.025x6.24     |

Now we divide the remaining open areas in rectangles and do the same verification that was used previously for the rooms of the level.
The open areas will be identified with letters in the schematic plan.

| Open Areas | Dimensions ($px$) | Dimensions ($m$) | Area ($m²$) | $D_a$ (Diagonal) | Number of Lines | Number of Access Points |
|------------|-------------------|------------------|-------------|------------------|-----------------|-------------------------|
| A          | 132x537           | 45.75x186.14     | 8515.91     | 191.68           | 4               | 16                      |
| B          | 121x100           | 41.94x34.66      | 1453.64     | 54.41            | 1               | 3                       |
| C          | 291x142           | 100.87x49.22     | 4964.82     | 112.24           | 1               | 13                      |
| D          | 56x385            | 19.41x133.45     | 2590.26     | 134.85           | 3               | 3                       |
| E          | 78x123            | 27.04x42.63      | 1152.72     | 50.48            | 1               | 3                       |
| F          | 262x35            | 90.81x12.13      | 1101.53     | 91.62            | 1               | 3                       |
| G          | 126x60            | 43.67x20.80      | 908.336     | 48.37            | 1               | 1                       |
| H          | 79x115            | 27.38x39.86      | 1091.37     | 48.36            | 1               | 1                       |
| I          | 205x346           | 71.06x119.93     | 8522.23     | 139.40           | 3               | 12                      |
| J          | 46x202            | 15.94x70.02      | 1116.12     | 71.71            | 2               | 2                       |

**Open Area A**
- $n_{lines} = 4$
- $y_1 = 23.27 m$
- $d_1 = 23.27m$
- $c_1 = 9.14 m$
- $y_2 = 69.80 m$
- $d_2 = 69.80m$
- $c_2 = 9.14 m$
- $y_3 = 116.34 m$
- $d_3 = 69.80m$
- $c_3 = 9.14 m$
- $y_4 = 162.87 m$
- $d_4 = 23.27m$
- $c_4 = 9.14 m$
- $n_{APs} = 4$
- $spacing = 9.15 m$

| Access Point | Position ($m$) |
|--------------|----------------|
| 1            | 9.14x23.27     |
| 2            | 18.29x23.27    |
| 3            | 27.44x23.27    |
| 4            | 36.59x23.27    |
| 5            | 9.14x69.80     |
| 6            | 18.29x69.80    |
| 7            | 27.44x69.80    |
| 8            | 36.59x69.80    |
| 9            | 9.14x116.34    |
| 10           | 18.29x116.34   |
| 11           | 27.44x116.34   |
| 12           | 36.59x116.34   |
| 13           | 9.14x162.87    |
| 14           | 18.29x162.87   |
| 15           | 27.44x162.87   |
| 16           | 36.59x162.87   |

**Open Area B**
- $n_{lines} = 1$
- $y = 17.33 m$
- $d = 17.33 m$
- $c = 18.02 m$
- $n_{APs} = 3$
- §spacing = 2.95 m$

| Access Point | Position ($m$) |
|--------------|----------------|
| 1            | 18.02x17.33    |
| 2            | 20.97x17.33    |
| 3            | 23.92x17.33    |

**Open Area C**
- $n_{lines} = 1$
- $y = 24.61 m$
- $d = 24.61 m$
- $c = 4.40 m$
- $n_{APs} = 13$
- $spacing = 7.67 m$

| Access Point | Position ($m$) |
|--------------|----------------|
| 1            | 4.40x24.61     |
| 2            | 12.07x24.61    |
| 3            | 19.74x24.61    |
| 4            | 27.41x24.61    |
| 5            | 35.08x24.61    |
| 6            | 42.75x24.61    |
| 7            | 50.42x24.61    |
| 8            | 58.09x24.61    |
| 9            | 65.76x24.61    |
| 10           | 73.43x24.61    |
| 11           | 81.10x24.61    |
| 12           | 88.77x24.61    |
| 13           | 96.44x24.61    |

**Open Area D**
- $n_{lines} = 3$
- $y_1 = 22.24 m$
- $d_1 = 22.24 m$
- $c_1 = 11.42 m$
- $y_2 = 66.705 m$
- $d_2 = 66.705 m$
- $c_2 = 11.41 m$
- $y_3 = 111.21 m$
- $d_3 = 22.24 m$
- $c_3 = 11.42 m$
- $n_{APs} = 2$
- $spacing = -3.43 m$

> $spacing < 0$ which means that realistically we only require a single access point per line to cover both corners of the area which will be positioned in the center of its respective line.

| Access Point | Position ($m$) |
|--------------|----------------|
| 1            | 9.71x22.24     |
| 2            | 9.71x66.705    |
| 3            | 9.71x111.21    |

**Open Area E**
- $n_{lines} = 1$
- $y = 21.315 m$
- $d = 21.315 m$
- $c = 13.06 m$
- $n_{APs} = 3$
- $spacing = 0.46 m$

| Access Point | Position ($m$) |
|--------------|----------------|
| 1            | 13.06x21.315   |
| 2            | 13.52x21.315   |
| 3            | 13.98x21.315   |

**Open Area F**
- $n_{lines} = 1$
- $y = 6.065 m$
- $d = 6.065 m$
- $c = 24.25 m$
- $n_{APs} = 3$
- $spacing = 21.155 m$

| Access Point | Position ($m$) |
|--------------|----------------|
| 1            | 24.25x6.065    |
| 2            | 45.405x6.065   |
| 3            | 66.56x6.065    |

**Open Area I**
- $n_{lines} = 3$
- $y_1 = 19.99 m$
- $d_1 = 19.99 m$
- $c_1 = 15.01 m$
- $y_2 = 59.97 m$
- $d_2 = 59.96 m$
- $c_2 = 15.01m$
- $y_3 = 99.94 m$
- $d_3 = 19.99 m$
- $c_3 = 15.01 m$
- $n_{APs} = 4$
- $spacing = 13.67 m$

| Access Point | Position ($m$) |
|--------------|----------------|
| 1            | 15.02x19.99    |
| 2            | 28.69x19.99    |
| 3            | 42.36x19.99    |
| 4            | 56.03x19.99    |
| 5            | 15.02x59.97    |
| 6            | 28.69x59.97    |
| 7            | 42.36x59.97    |
| 8            | 56.03x59.97    |
| 9            | 15.02x99.94    |
| 10           | 28.69x99.94    |
| 11           | 42.36x99.94    |
| 12           | 56.03x99.94    |

**Open Area J**
- $n_{lines} = 2$
- $y_1 = 17.51 m$
- $d_1 = 17.51 m$
- $c_1 = 17.84 m$
- $y_2 = 52.51 m$
- $d_2 = 17.51 m$
- $c_2 = 17.84 m$
- $n_{APs} = 2$

> Despite being mathematically correct, as c > length of the area, we only require 1 access point per line to cover both corners. Each access point will be placed in the center of its respective line.

| Access Point | Position ($m$) |
|--------------|----------------|
| 1            | 7.97x17.51     |
| 2            | 7.97x52.51     |

---