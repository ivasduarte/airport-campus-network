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

**Total standard outlets for Level 1: 936**

---