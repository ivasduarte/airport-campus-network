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

#### 2.1.3. Access Points Calculations and Positions

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

---

| Space | Length ($m$) | Width ($m$) | $Length^2 \times Width^2$ | AP Quantity |
|-------|--------------|-------------|---------------------------|-------------|
| 1     | 28.8         | 18.3        | 1164.33                   | 1           |
| 2     | 49.1         | 129.5       | 19181.06                  | 6           |

---

**Extra Calculations for Space 2 AP Amount**

* To calculate the amount of APs needed for this space we will follow some rules.
* **1.** If some measurement is less than 90% of 50$m$ (around 45$m$) we can fill the room with only one line of APs.
  Otherwise, we should add one extra line;
* **2.** To get the number of lines needed we can use the formula: $n = H \div diameter$;
* **3.** The first APs to be placed must be the ones that cover the corners;
*
* As the space length is less than the AP diameter but greater than 45$m$ we will add two lines of APs to optimize
  space.
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

* **E8** <br>
    * As both measurements are greater than 45$m$, we will need more than one line of APs.
    * As the subspace length is 173.1$m$, and $173.1 \div 50 = 3.5$, we will need 4 lines of APs
    * If we make $173.1 \div 8$, we get the distance the outside lines must have from the wall, which is 21.64$m$
    * With that, we can calculate the maximum $y$ distance the first and last APs should be placed from the wall. <br>
    * $y = \sqrt{25^2 - 21.64^2} = 12.52m$
    * **Maximum distance between 2 APs:** $2 * y = 25.04m$
    * **Between First and Last APs of a line:** $84.46 \div 25.04 = 3.37$, which means that we need 3 more APs per line

---

##### APs Positions (ToDo)

| AP   | X ($m$) | Y ($m$) |
|------|---------|---------|
| AP1  |         |         |
| AP2  |         |         |
| AP3  |         |         |
| AP4  |         |         |
| AP5  |         |         |
| AP6  |         |         |
| AP7  |         |         |
| AP8  |         |         |
| AP9  |         |         |
| AP10 |         |         |
| AP11 |         |         |
| AP12 |         |         |
| AP13 |         |         |
| AP14 |         |         |
| AP15 |         |         |
| AP16 |         |         |
| AP17 |         |         |
| AP18 |         |         |
| AP19 |         |         |
| AP20 |         |         |
| AP21 |         |         |
| AP22 |         |         |
| AP23 |         |         |
| AP24 |         |         |
| AP25 |         |         |
| AP26 |         |         |
| AP27 |         |         |
| AP28 |         |         |
| AP29 |         |         |
| AP30 |         |         |
| AP31 |         |         |
| AP32 |         |         |
| AP33 |         |         |
| AP34 |         |         |
| AP35 |         |         |
| AP36 |         |         |
| AP37 |         |         |
| AP38 |         |         |
| AP39 |         |         |
| AP40 |         |         |
| AP41 |         |         |
| AP42 |         |         |
| AP43 |         |         |
| AP44 |         |         |
| AP45 |         |         |
| AP46 |         |         |
| AP47 |         |         |
| AP48 |         |         |
| AP49 |         |         |
| AP50 |         |         |
| AP51 |         |         |
| AP52 |         |         |
| AP53 |         |         |
| AP54 |         |         |

---

#### 2.1.4. Schematic Plans

##### Outlets (ToDo)

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

#### 2.2.3. Access Points Calculations and Positions

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
| 1    | 20.95        | 11.4        | 568.86                    | 1           | 
| 2    | 26.7         | 11.4        | 842.85                    | 1           |
| 3    | 19.05        | 11.4        | 492.86                    | 1           |
| 4    | 19.05        | 11.4        | 492.86                    | 1           |
| 5    | 38.1         | 13.3        | 1628.5                    | 1           |
| 6    | 34.3         | 13.3        | 1353.38                   | 1           |
| 7    | 36.2         | 13.3        | 1487.33                   | 1           |
| 8    | 7.17         | 13.3        | 228.3                     | 1           |
| 9    | 13.3         | 19.05       | 539.79                    | 1           |
| 10   | 26.7         | 15.2        | 943.93                    | 1           |
| 11   | 13.3         | 19.05       | 539.79                    | 1           |
| 12   | 13.3         | 19.05       | 539.79                    | 1           |
| 13   | 13.3         | 19.05       | 539.79                    | 1           |
| 14   | 13.3         | 13.3        | 353.78                    | 1           |
| 15   | 26.7         | 18.04       | 1038.33                   | 1           |
| 16   | 27.0         | 18.04       | 1054.44                   | 1           |
| 17   | 10.0         | 10.0        | 200.00                    | 1           |
| 18   | 9.35         | 10.0        | 187.42                    | 1           |

---

> Other than the predefined rooms, I've divided the remaining of the floor in three distinct spaces. <br>
> **1.** Corridor right below room 14. <br>
> **2.** Space above room 10. <br>
> **3.** Space to the bottom left of room 10. <br>
> **4.** Space right below and to bottom right of room 10. <br>
> **5.** Remaining of the floor.
>
> All the above spaces (except for Space 5) are shown in the schematic
> (labeled as "S$x$", where $x$ is the number of the space).
>
> NOTE: The spaces on the sides of room 10 won't be calculated as
> their size will be covered by the APs of the spaces around.

---

| Space | Length ($m$) | Width ($m$) | $Length^2 \times Width^2$ | AP Quantity |
|-------|--------------|-------------|---------------------------|-------------|
| 1     | 21.5         | 42.6        | 2277.01                   | 1           |
| 2     | 23.9         | 83.0        | 7460.21                   | 2           |
| 3     | 82.6         | 17.8        | 7139.60                   | 2           |
| 4     | 122.0        | 63.3        | 18890.9                   | 8           |

---

> To calculate the amount of APs needed for spaces with more than one AP we will follow some rules. <br>
> **1.** If some measurement is less than 90% of 50$m$ (around 45$m$) we can fill the room with only one line of APs.
> Otherwise, we should add one extra line; <br>
> **2.** To get the number of lines needed we can use the formula: $n = H \div diameter$; <br>
> **3.** The first APs to be placed must be the ones that cover the corners; <br>

**Extra Calculations for Space 2 AP Amount**

* As the space length is less than 45$m$, only one line of APs will be needed.
* Making $23.9 \div 2$ we get the distance the outside APs must have from the wall, which is 11.95$m$
* With that, we can calculate the maximum $x$ distance the first and last APs should be placed from the wall. <br>
* $x = \sqrt{25^2 - 11.95^2} = 21.96m$
* **Maximum distance between 2 APs:** $2 * x = 43.92m$
* **Between First and Last APs of a line:** $39.08 \div 43.92 = 0.89$, which means no intermediate AP is needed.

**Extra Calculations for Space 3 AP Amount**

* As the space width is less than 45$m$, only one line of APs will be needed.
* Making $17.8 \div 2$ we get the distance the outside lines must have from the wall, which is 8.9$m$
* With that, we can calculate the maximum $y$ distance the first and last APs should be placed from the wall. <br>
* $y = \sqrt{25^2 - 8.9^2} = 23.36m$
* **Maximum distance between 2 APs:** $2 * y = 46.72m$
* **Between First and Last APs of a line:** $35.88 \div 46.72 = 0.77$, which means no intermediate AP is needed.

**Extra Calculations for Space 4 AP Amount**

* As both measurements are greater than 45$m$, we will need more than one line of APs.
* As the space width is 63.3$m$, and $63.3 \div 50 = 1.3$, we will need 2 lines of APs
* Making $63.3 \div 4$ we get the distance the outside lines must have from the wall, which is 15.83$m$
* With that, we can calculate the maximum $y$ distance the first and last APs should be placed from the wall. <br>
* $y = \sqrt{25^2 - 15.83^2} = 19.35m$
* **Maximum distance between 2 APs:** $2 * y = 38.7m$
* **Between First and Last APs of a line:** $83.3 \div 38.7 = 2.15$, which means that we need 2 more APs per line.

> **Note:** As **Space 5** is not in a rectangular shape we can't apply the same logic.

**Calculations for Space 5**

> In order to make the calculation of Space 5 APs, we proceeded with its
> division in multiple rectangular shaped subspaces
> (shown in the schematic as "E$x$", with $x$ being the number given to the subspace).

> **Note:** The space between Space 1 and the wall will not be considered as the AP in Space 1 covers it.

---

| Subspace | Length ($m$) | Width ($m$) | $Length^2 \times Width^2$ | AP Quantity |
|----------|--------------|-------------|---------------------------|-------------|
| 1        | 90.87        | 102.83      | 18831.4                   | 9           |
| 2        | 20.87        | 60.43       | 4087.34                   | 2           |
| 3        | 43.48        | 116.96      | 15570.2                   | 5           |
| 4        | 26.52        | 181.74      | 33732.7                   | 5           |

---

**Extra Calculations for Subspaces that need more than one AP**

* **E1** <br>
    * As both measurements are greater than 45$m$, we will need more than one line of APs.
    * As the subspace width is 102.83$m$, and $102.83 \div 50 = 2.1$, we will need 3 lines of APs
    * If we make $102.83 \div 6$, we get the distance the outside lines must have from the wall, which is 17.14$m$
    * With that, we can calculate the maximum $y$ distance the first and last APs should be placed from the wall.
    * $y = \sqrt{25^2 - 17.14^2} = 18.2m$
    * **Maximum distance between 2 APs:** $2 * y = 36.4m$
    * **Between First and Last APs of a line:** $54.47 \div 36.4 = 1.5$, which means that we need 1 more APs per line.

* **E2** <br>
    * As the subspace length is 20.87$m$, only one line of APs will be needed.
    * Making $20.87 \div 2$ we get the distance the outside APs must have from the wall, which is 10.44$m$
    * With that, we can calculate the maximum $x$ distance the first and last APs should be placed from the wall. <br>
    * $x = \sqrt{25^2 - 10.44^2} = 22.72m$
    * **Maximum distance between 2 APs:** $2 * x = 45.44m$
    * **Between First and Last APs of a line:** $14.99 \div 45.44 = 0.33$, which means no intermediate AP is needed.

* **E3** <br>
    * As the subspace length is 43.48$m$, only one line of APs will be needed.
    * Making $43.48 \div 2$ we get the distance the outside APs must have from the wall, which is 21.74$m$
    * With that, we can calculate the maximum $x$ distance the first and last APs should be placed from the wall. <br>
    * $x = \sqrt{25^2 - 21.74^2} = 12.34m$
    * **Maximum distance between 2 APs:** $2 * x = 24.68m$
    * **Between First and Last APs of a line:** $92.28 \div 24.68 = 3.74$, which means that we need 3 more APs.

* **E4** <br>
    * As the subspace length is 26.52$m$, only one line of APs will be needed.
    * Making $26.52 \div 2$ we get the distance the outside APs must have from the wall, which is 13.26$m$
    * With that, we can calculate the maximum $x$ distance the first and last APs should be placed from the wall. <br>
    * $x = \sqrt{25^2 - 13.26^2} = 21.19m$
    * **Maximum distance between 2 APs:** $2 * x = 42.38m$
    * **Between First and Last APs of a line:** $139.36 \div 42.38 = 3.29$, which means that we need 3 more APs.

---

##### APs Positions

| AP   | X ($m$) | Y ($m$) |
|------|---------|---------|
| AP1  | 10.87   | 5.22    |
| AP2  | 33.48   | 5.22    |
| AP3  | 54.13   | 5.22    |
| AP4  | 73.7    | 5.22    |
| AP5  | 103.26  | 6.74    |
| AP6  | 139.78  | 6.74    |
| AP7  | 174.78  | 6.74    |
| AP8  | 197.17  | 6.74    |
| AP9  | 90.65   | 23.48   |
| AP10 | 33.26   | 42.83   |
| AP11 | 90.65   | 42.83   |
| AP12 | 90.65   | 62.17   |
| AP13 | 90.65   | 82.0    |
| AP14 | 90.65   | 98.7    |
| AP15 | 9.13    | 147.61  |
| AP16 | 9.13    | 175.43  |
| AP17 | 5.0     | 194.78  |
| AP18 | 195.43  | 194.78  |
| AP19 | 107.83  | 116.96  |
| AP20 | 22.17   | 23.26   |
| AP21 | 61.09   | 23.26   |
| AP22 | 9.13    | 73.91   |
| AP23 | 9.13    | 109.57  |
| AP24 | 35.65   | 69.57   |
| AP25 | 66.96   | 69.57   |
| AP26 | 35.65   | 97.39   |
| AP27 | 66.96   | 97.39   |
| AP28 | 35.65   | 125.0   |
| AP29 | 66.96   | 125.0   |
| AP30 | 35.65   | 152.83  |
| AP31 | 66.96   | 152.83  |
| AP32 | 115.22  | 32.39   |
| AP33 | 149.57  | 32.39   |
| AP34 | 183.7   | 32.39   |
| AP35 | 115.22  | 59.57   |
| AP36 | 149.57  | 59.57   |
| AP37 | 183.7   | 59.57   |
| AP38 | 115.22  | 86.52   |
| AP39 | 149.57  | 86.52   |
| AP40 | 183.7   | 86.52   |
| AP41 | 163.26  | 116.74  |
| AP42 | 178.04  | 116.74  |
| AP43 | 96.3    | 150.0   |
| AP44 | 119.35  | 150.0   |
| AP45 | 142.39  | 150.0   |
| AP46 | 165.43  | 150.0   |
| AP47 | 188.48  | 150.0   |
| AP48 | 40.43   | 186.52  |
| AP49 | 75.22   | 186.52  |
| AP50 | 110.0   | 186.52  |
| AP51 | 144.78  | 186.52  |
| AP52 | 179.57  | 186.52  |

---

#### 2.2.4. Schematic Plans

##### Outlets (ToDo)

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