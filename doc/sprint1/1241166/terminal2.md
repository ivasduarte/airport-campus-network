# Terminal 2

---

## 1. Measurements

* **Building Dimensions:** $200m \times 200m = 40000m^2$

---

## 2. Network Outlet Calculations

**Standard Rule:** 2 outlets every 10$m^2$ → `outlets = area / 10 × 2`
> When calculating "(area / 10)", the result will always be
> rounded **up** to ensure full area coverage.

--- 

### 2.1. Level 1 (Arrivals)

> Rooms **with** standard outlets : 1, 2, 3, 4, 5, 7, 8 <br>
> Rooms **without** outlets : 6, 9, 10, 11, 12

---

#### 2.1.1. Room Areas & Outlet Calculations

| Room | Length ($m$) | Width ($m$) | Area ($m^2$) | Outlets | 
|------|--------------|-------------|--------------|---------|
| 1    | 27.3         | 10.6        | 289.38       | 58      | 
| 2    | 22.7         | 10.6        | 240.62       | 49      |
| 3    | 33.3         | 10.6        | 352.98       | 71      |
| 4    | 37.9         | 10.6        | 401.74       | 81      |
| 5    | 30.3         | 10.6        | 321.18       | 65      |
| 7    | 28.8         | 15.1        | 434.88       | 87      |
| 8    | 28.8         | 16.7        | 480.96       | 97      |

**Total Standard outlets for Level 1: 508**

---

#### 2.1.2. External Wall

> As stated on the project requirements, there must be 1 outlet every 5 meters along the **right** and **bottom**
> external walls of Level 1.

| Wall   | Real Length ($m$) | Outlets (length / 5) |
|--------|-------------------|----------------------|
| Right  | 200               | **40**               |
| Bottom | 200               | **40**               |

**Total standard outlets for external walls on Level 1: 80**
**Total standard outlets for Level 2: 588**

---

#### 2.1.3. Access Points Calculations and Positions (ToDo)

> Access Points need to be calculated for each room, individually. <br>
> For that, we can use an adaptation of the Pythagorean theorem, such as:
> $Length^2 \times Width^2 \leq Diameter^2$
>
> **First Equation Member:** Room Measurements <br>
> **Second Equation Member:** AP Diameter
>
> If the condition above turns out **true**, it means that an AP in the middle of the room is enough for full
> coverage. <br>
> Otherwise, some other calculations need to be made.

---

##### APs needed per room

**Diameter Squared of AP:** 2500

| Room | Length ($m$) | Width ($m$) | $Length^2 \times Width^2$ | AP Quantity |
|------|--------------|-------------|---------------------------|-------------|
| 1    | 27.3         | 10.6        | 857.65                    | 1           |
| 2    | 22.7         | 10.6        | 627.65                    | 1           |
| 3    | 33.3         | 10.6        | 1221.25                   | 1           |
| 4    | 37.9         | 10.6        | 1548.77                   | 1           |
| 5    | 30.3         | 10.6        | 1030.45                   | 1           |
| 6    | 7.4          | 10.1        | 156.77                    | 1           |
| 7    | 28.8         | 15.1        | 1057.45                   | 1           |
| 8    | 28.8         | 16.7        | 1108.33                   | 1           |
| 9    | 24.0         | 18.3        | 910.89                    | 1           |
| 10   | 24.0         | 18.3        | 910.89                    | 1           |
| 11   | 10.1         | 10.1        | 204.02                    | 1           |
| 12   | 10.5         | 10.1        | 212.26                    | 1           |

---

##### APs Positions (ToDo)

| AP   | X ($m$) | Y ($m$) |
|------|---------|---------|
| AP1  | 25      | 25      |
| AP2  | 25      | 75      |
| AP3  | 25      | 125     |
| AP4  | 25      | 175     |
| AP5  | 75      | 25      |
| AP6  | 75      | 75      |
| AP7  | 75      | 125     |
| AP8  | 75      | 175     |
| AP9  | 125     | 25      |
| AP10 | 125     | 75      |
| AP11 | 125     | 125     |
| AP12 | 125     | 175     |
| AP13 | 175     | 25      |
| AP14 | 175     | 75      |
| AP15 | 175     | 125     |
| AP16 | 175     | 175     |

---

#### 2.1.4. Schematic Plans (ToDo)

##### Outlets

> This schematic shows an example layout for the outlets on the Level. The plan **is not** drawn to scale, as doing so
> would make the diagram too difficult to read.
>
> When placing the outlets, no point in each room can be more than 3 meters away from one.

![Network Outlets Deployment schematic Plan Level 1](assets/EsquemaOutletsLevel1.jpg) (ToDo) <br>
**(For clarity, outlets associated with Access Points will be shown on a separate schematic)**

##### Access Points

> This floor requires LAN coverage (Wi-Fi).
>
> Each Access Point covers a circle of 50$m$ diameter. <br>
> All APs will be installed in the space above the dropped ceiling. <br>
> Each AP will require **a dedicated outlet**.
>
> This schematic shows how to place the APs and their Dedicated Outlets. Because each level requires 16 APs in the exact
> same positions, this schematic applies to all levels.

![Access Points Schematic](assets/EsquemaAPLevel1.jpg)

---

### 2.2. Level 4 (Departures)

> Rooms **with** standard outlets : 1, 2, 3, 4, 5, 7, 9, 10, 11, 12, 13, 14 <br>
> Rooms **without** outlets : 8, 15, 16, 17, 18

---

#### 2.2.1. Room Areas & Outlet Calculations

| Room | Length ($m$) | Width ($m$) | Area ($m^2$) | Outlets | 
|------|--------------|-------------|--------------|---------|
| 1    | 20.95        | 11.4        | 238.83       | 48      | 
| 2    | 26.7         | 11.4        | 304.38       | 61      |
| 3    | 19.05        | 11.4        | 217.17       | 44      |
| 4    | 19.05        | 11.4        | 217.17       | 44      |
| 5    | 38.1         | 13.3        | 506.73       | 102     |
| 6    | 34.3         | 13.3        | 456.19       | 92      |
| 7    | 36.2         | 13.3        | 481.46       | 97      |
| 9    | 13.3         | 19.05       | 253.37       | 51      |
| 10   | 26.7         | 15.2        | 405.84       | 82      |
| 11   | 13.3         | 19.05       | 253.37       | 51      |
| 12   | 13.3         | 19.05       | 253.37       | 51      |
| 13   | 13.3         | 19.05       | 253.37       | 51      |
| 14   | 13.3         | 13.3        | 176.89       | 36      |

**Total Standard outlets for Level 4: 810**

---

#### 2.2.2. External Wall

> As stated on the project requirements, there must be 1 outlet every 5 meters along the **right** and **bottom**
> external walls of Level 4.

| Wall   | Real Length ($m$) | Outlets (length / 5) |
|--------|-------------------|----------------------|
| Right  | 200               | **40**               |
| Bottom | 200               | **40**               |

**Total standard outlets for external walls on Level 4: 80**
**Total standard outlets for Level 2: 890**

---

#### 2.2.3. Access Points Calculations and Positions (ToDo)

> Access Points need to be calculated for each room, individually. <br>
> For that, we can use an adaptation of the Pythagorean theorem, such as:
> $Length^2 \times Width^2 \leq Diameter^2$
>
> **First Equation Member:** Room Measurements <br>
> **Second Equation Member:** AP Diameter
>
> If the condition above turns out **true**, it means that an AP in the middle of the room is enough for full
> coverage. <br>
> Otherwise, some other calculations need to be made.

---

##### APs needed per room (ToDo)

| Room | Length ($m$) | Width ($m$) | $Length^2 \times Width^2$ | AP Quantity | 
|------|--------------|-------------|---------------------------|-------------|
| 1    | 20.95        | 11.4        |                           |             | 
| 2    | 26.7         | 11.4        |                           |             |
| 3    | 19.05        | 11.4        |                           |             |
| 4    | 19.05        | 11.4        |                           |             |
| 5    | 38.1         | 13.3        |                           |             |
| 6    | 34.3         | 13.3        |                           |             |
| 7    | 36.2         | 13.3        |                           |             |
| 8    |              |             |                           |             |
| 9    | 13.3         | 19.05       |                           |             |
| 10   | 26.7         | 15.2        |                           |             |
| 11   | 13.3         | 19.05       |                           |             |
| 12   | 13.3         | 19.05       |                           |             |
| 13   | 13.3         | 19.05       |                           |             |
| 14   | 13.3         | 13.3        |                           |             |
| 15   |              |             |                           |             |
| 16   |              |             |                           |             |
| 17   |              |             |                           |             |
| 18   |              |             |                           |             |

---

##### APs Positions (ToDo)

| AP   | X ($m$) | Y ($m$) |
|------|---------|---------|
| AP1  | 25      | 25      |
| AP2  | 25      | 75      |
| AP3  | 25      | 125     |
| AP4  | 25      | 175     |
| AP5  | 75      | 25      |
| AP6  | 75      | 75      |
| AP7  | 75      | 125     |
| AP8  | 75      | 175     |
| AP9  | 125     | 25      |
| AP10 | 125     | 75      |
| AP11 | 125     | 125     |
| AP12 | 125     | 175     |
| AP13 | 175     | 25      |
| AP14 | 175     | 75      |
| AP15 | 175     | 125     |
| AP16 | 175     | 175     |

---

#### 2.2.4. Schematic Plans (ToDo)

##### Outlets

> This schematic shows an example layout for the outlets on the Level. The plan **is not** drawn to scale, as doing so
> would make the diagram too difficult to read.
>
> When placing the outlets, no point in each room can be more than 3 meters away from one.

![Network Outlets Deployment schematic Plan Level 4](assets/EsquemaOutletsLevel4.jpg) (ToDo) <br>
**(For clarity, outlets associated with Access Points will be shown on a separate schematic)**

---

##### Access Points

> This floor requires LAN coverage (Wi-Fi).
>
> Each Access Point covers a circle of 50$m$ diameter. <br>
> All APs will be installed in the space above the dropped ceiling. <br>
> Each AP will require **a dedicated outlet**.
>
> This schematic shows how to place the APs and their Dedicated Outlets. Because each level requires 16 APs in the exact
> same positions, this schematic applies to all levels.

![Access Points Schematic](assets/EsquemaAPLevel4.jpg)

---

## 4. MC, HC and CP (ToDo)