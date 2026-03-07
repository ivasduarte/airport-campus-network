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
> For that, we can use an adaptation of the Pythagorean theorem, such as, as all the rooms have a rectangular shape:
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

> Other than the predefined rooms, I've divided the remaining of the floor in three distinct spaces. <br>
> **1.** Space between rooms 7 and 8, with the exact same length of these rooms. <br>
> **2.** Space between rooms on the far left of the floor (1 & 2 --> 9 & 10). <br>
> **3.** Remaining of the floor
>
> All the above spaces (except for Space 3) are shown in the schematic
> (labeled as "S$x$", where $x$ is the number of the space)

| Space | Length ($m$) | Width ($m$) | $Length^2 \times Width^2$ | AP Quantity |
|-------|--------------|-------------|---------------------------|-------------|
| 1     | 28.8         | 18.3        | 1164.33                   | 1           |
| 2     | 49.1         | 129.5       | 19181.06                  | 6           |

**Extra Calculations for Space 2 AP Amount** (ToDo)

* To calculate the amount of APs needed for this space we will follow some rules.
* **1.** If some measurement is less than 90% of 50$m$ (around 45$m$) we can fill the room with only one line of APs.
  Otherwise, we should add one extra line;
* **2.** To get the number of lines needed we can use the formula: $n = H \div diameter$;
* **3.** The first APs to be placed must be the ones that cover the corners;
*
* As the space length is less than the AP diameter but greater than 45$m$ we will add two lines of APs to optimize space.
* Making $49.1 \div 4$ we get the distance the outside lines must have from the wall, which is 12.28$m$
* With that, we can calculate the maximum $y$ distance the first and last APs should be placed from the wall. <br>
* $y = \sqrt{25^2 - 12.28^2} = 21.78m$
* **Maximum distance between 2 APs:** $2 * y = 43.56m$
* **Between First and Last APs of a line:** $85.94 \div 43.56 = 1.97$, which means that we need 1 more APs per line

> **Note:** As **Space 3** is not in a rectangular shape we can't apply the same logic.

**Calculations for Space 3**

> In order to make the calculation of Space 3 APs, we proceeded with its
> division in multiple rectangular shaped subspaces
> (shown in the schematic as "E$x$", with $x$ being the number given to the subspace).

---

| Subspace | Length ($m$) | Width ($m$) | $Length^2 \times Width^2$ | AP Quantity |
|----------|--------------|-------------|---------------------------|-------------|
| 1        | 24.0         | 9.9         | 674.01                    | 1           |
| 2        | 24.0         | 37.9        | 2012.41                   | 1           |
| 3        | 56.8         | 26.7        | 3939.13                   | 2           |
| 4        | 9.7          | 176.6       | 31281.65                  | 4           |
| 5        | 62.7         | 26.7        | 4644.18                   | 2           |
| 6        | 10.3         | 33.1        | 1201.7                    | 1           |
| 7        | 175.6        | 10.5        | 30945.61                  | 4           |
| 8        | 173.1        | 109.5       | 41953.86                  | 20          |

---

**Extra Calculations for Subspaces that need more than one AP**

* **E3** <br>
    * As the subspace width is 26.7$m$, only one line of APs will be needed. <br>
    * $26.7 \div 2 = 13.35m$, which makes the center of the width of the room. <br>
    * With that, we can calculate the maximum $x$ distance the first and last APs should be placed from the wall. <br>
    * $x = \sqrt{25^2 - 13.35^2} = 21.14m$
    * **Maximum distance between 2 APs:** $2 * x = 42.28m$
    * **Between First and Last APs:** $14.52 \div 42.28 = 0.34$, which means no intermediate AP is needed

* **E4** <br>
    * As the subspace length is 9.7$m$, only one line of APs will be needed. <br>
    * $9.7 \div 2 = 4.85m$, which makes the center of the length of the room. <br>
    * With that, we can calculate the maximum $y$ distance the first and last APs should be placed from the wall. <br>
    * $y = \sqrt{25^2 - 4.85^2} = 24.5m$
    * **Maximum distance between 2 APs:** $2 * y = 49m$
    * **Between First and Last APs:** $127.6 \div 49 = 2.6$, which means that we need 2 more APs for full coverage

* **E5** <br>
    * As the subspace width is 26.7$m$, only one line of APs will be needed. <br>
    * $26.7 \div 2 = 13.35m$, which makes the center of the width of the room. <br>
    * With that, we can calculate the maximum $x$ distance the first and last APs should be placed from the wall. <br>
    * $x = \sqrt{25^2 - 13.35^2} = 21.14m$
    * **Maximum distance between 2 APs:** $2 * x = 42.28m$
    * **Between First and Last APs:** $20.42 \div 42.28 = 0.48$, which means no intermediate AP is needed

* **E7** <br>
    * As the subspace width is 10.5$m$, only one line of APs will be needed. <br>
    * $10.5 \div 2 = 5.25m$, which makes the center of the width of the room. <br>
    * With that, we can calculate the maximum $x$ distance the first and last APs should be placed from the wall. <br>
    * $x = \sqrt{25^2 - 5.25^2} = 24.44m$
    * **Maximum distance between 2 APs:** $2 * x = 48.88m$
    * **Between First and Last APs:** $126.72 \div 48.88 = 2.59$, which means that we need 2 more APs for full coverage

* **E8** (Incorrect schematic) <br>
    * As both measurements are greater than 45$m$, we will need more than one line of APs.
    * As the subspace length is $173.1$, and $173.1 \div 50 = 3.5$, we will need 4 lines of APs
    * If we make $173.1 \div 8$, we get the distance the outside lines must have from the wall, which is 21.64$m$
    * With that, we can calculate the maximum $y$ distance the first and last APs should be placed from the wall. <br>
    * $y = \sqrt{25^2 - 21.64^2} = 12.52m$
    * **Maximum distance between 2 APs:** $2 * y = 25.04m$
    * **Between First and Last APs of a line:** $84.46 \div 25.04 = 3.37$, which means that we need 3 more APs per line

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

![Network Outlets Deployment Schematic Plan Level 1](assets/EsquemaOutletsLevel1.jpg) (ToDo) <br>
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

![Access Points Schematic Level 1](assets/EsquemaAPLevel1.jpg)

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

![Network Outlets Deployment Schematic Plan Level 4](assets/EsquemaOutletsLevel4.jpg) (ToDo) <br>
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

![Access Points Schematic Level 4](assets/EsquemaAPLevel4.jpg)

---

## 4. MC, HC and CP (ToDo)