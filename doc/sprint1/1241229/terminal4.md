# Terminal 4 

---

## 1. Scale & Measurements

* **Building dimensions:** 200$m$ × 100$m$ = 20000 $m^2$;
* **Scale Used:** 2.9$cm$ = 50$m$ → 1$cm$ = 17.2414$m$;

---

## 2. Network Outlets  Calculation

**Standard rule:** 2 outlets per every 10 $m^2$ → `outlets = area / 10 × 2`
> When calculating "(area/10)", the result will always be rounded **up** to ensure full area coverage.

---

### 2.1. Level 0 (Arrivals)

> Rooms **with** standard outlets : 1, 2, 3, 5, 6, 7, 12, 13, 14, 15, 16
> 
> Rooms **without** outlets : 4 (IC), 8, 9, 10, 11

---

#### 2.1.1. Room Areas & Outlet Calculation

| Room | Dimensions ($cm$) | Length ($m$) | Width ($m$) | Area ($m^2$) | (Area / 10) (rounded up) | Outlets (x2) |
|------|-------------------|--------------|-------------|--------------|--------------------------|--------------|
| 1    | 1.9 × 0.7         | 32.76        | 12.07       | 395.4        | 40                       | **80**       |
| 2    | 1.8 × 0.7         | 31.03        | 12.07       | 374.5        | 38                       | **76**       |
| 3    | 1.5 × 0.7         | 25.86        | 12.07       | 312.1        | 32                       | **64**       |
| 4    | 0.6 × 0.7         | 10.34        | 12.07       | 124.8        | -                        | -            |
| 5    | 1.2 × 0.7         | 20.69        | 12.07       | 249.7        | 25                       | **50**       |
| 6    | 1.7 × 0.7         | 29.31        | 12.07       | 353.8        | 36                       | **72**       |
| 7    | 1.5 × 0.7         | 25.86        | 12.07       | 312.1        | 32                       | **64**       |
| 8    | 1.5 × 0.7         | 25.86        | 12.07       | 312.1        | -                        | -            |
| 9    | 1.5 × 0.7         | 25.86        | 12.07       | 312.1        | -                        | -            |
| 10   | 0.8 × 1.3         | 13.79        | 22.41       | 309.0        | -                        | -            |
| 11a  | 0.7 × 0.7         | 12.07        | 12.07       | 145.7        | -                        | -            |
| 11b  | 0.8 × 0.6         | 13.79        | 10.34       | 142.6        | -                        | -            |
| 12   | 1.5 × 0.8         | 25.86        | 13.79       | 356.6        | 36                       | **72**       |
| 13   | 1.3 × 0.8         | 22.41        | 13.79       | 309.0        | 31                       | **62**       |
| 14   | 1.8 × 0.8         | 31.03        | 13.79       | 427.9        | 43                       | **86**       |
| 15   | 1.3 × 0.8         | 22.41        | 13.79       | 309.0        | 31                       | **62**       |
| 16   | 1.3 × 0.8         | 22.41        | 13.79       | 309.0        | 31                       | **62**       |

**Total standard outlets for Level 0: 750**

---

#### Schematic Plan (For Standard Outlets Only)
>This schematic shows an example layout for the outlets on the Level. The plan **is not** drawn to scale, as doing so would make the diagram too difficult to read. 
>
>When placing the outlets, no point in each room can be more than 3 meters away from one.
>
>**Red** represents **4** outlets and **Yellow** represents **2** outlets.

![Network Outlets Deployment schematic Plan Level 0](assets/Level0.png)

**(For clarity, outlets associated with Access Points will be shown on a separate schematic)**

---

### 2.2. Level 2 (Departures)


> Rooms **with** standard outlets: 1, 2, 4, 5, 7, 9, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21
> 
> Rooms **without** outlets: 3, 6, 8, 10, 11

---

#### 2.2.1. Room Areas & Outlet Calculation

| Room | Dimensions ($cm$) | Length ($m$) | Width ($m$) | Area ($m^2$) | (Area / 10) (rounded up) | Outlets (x2) |
|------|-------------------|--------------|-------------|--------------|--------------------------|--------------|
| 1    | 1.9 × 0.7         | 32.76        | 12.07       | 395.4        | 40                       | **80**       |
| 2    | 1.8 × 0.7         | 31.03        | 12.07       | 374.9        | 38                       | **76**       |
| 3    | 0.6 × 0.7         | 10.34        | 12.07       | 124.8        | -                        | -            |
| 4    | 1.2 × 0.7         | 20.69        | 12.07       | 249.7        | 25                       | **50**       |
| 5    | 1.5 × 0.7         | 25.86        | 12.07       | 312.4        | 32                       | **64**       |
| 6    | 1.5 × 0.6         | 25.86        | 10.34       | 267.4        | -                        | -            |
| 7    | 0.7 × 1.0         | 12.07        | 17.24       | 208.0        | 21                       | **42**       |
| 8    | 1.5 × 0.6         | 25.86        | 10.34       | 267.4        | -                        | -            |
| 9    | 0.7 × 1.0         | 12.07        | 17.24       | 208.0        | 21                       | **42**       |
| 10   | 0.8 × 1.3         | 13.79        | 22.41       | 309.0        | -                        | -            |
| 11a  | 0.7 × 0.6         | 12.07        | 10.34       | 124.8        | -                        | -            |
| 11b  | 0.8 × 0.7         | 13.79        | 12.07       | 166.4        | -                        | -            |
| 12   | 1.5 × 0.5         | 25.86        | 8.62        | 222.9        | 23                       | **46**       |
| 13   | 1.0 × 0.5         | 17.24        | 8.62        | 148.6        | 15                       | **30**       |
| 14   | 1.2 × 0.5         | 20.69        | 8.62        | 178.3        | 18                       | **36**       |
| 15   | 1.2 × 0.5         | 20.69        | 8.62        | 178.3        | 18                       | **36**       |
| 16   | 1.3 × 0.5         | 22.41        | 8.62        | 193.2        | 20                       | **40**       |
| 17   | 1.5 × 0.7         | 25.86        | 12.07       | 312.4        | 32                       | **64**       |
| 18   | 1.3 × 0.7         | 22.41        | 12.07       | 270.7        | 28                       | **56**       |
| 19   | 1.8 × 0.7         | 31.03        | 12.07       | 374.9        | 38                       | **76**       |
| 20   | 1.3 × 0.7         | 22.41        | 12.07       | 270.7        | 28                       | **56**       |
| 21   | 1.3 × 0.7         | 22.41        | 12.07       | 270.7        | 28                       | **56**       |

**Total standard outlets for Level 2 (excluding external walls): 850**

---


#### 2.2.2. External Wall (Level 2 only)

> As stated on the project requirements, there must be 1 outlet every 5 meters along the **right** and **bottom** external walls of Level 2.

| Wall   | Length ($m$) | Outlets (length / 5) |
|--------|--------------|----------------------|
| Right  | 100          | **20**               |
| Bottom | 200          | **40**               |

However, one outlet will be placed at the corner, meaning it will be a part of both walls, since they form a 90º angle with each other, which means:

**Total standard outlets for external walls on Level 2: 59**

**Total standard outlets for Level 2: 909**

---

#### Schematic Plan (For Standard Outlets Only)
>This schematic shows an example layout for the outlets on the Level. The plan **is not** drawn to scale, as doing so would make the diagram too difficult to read.
>
>When placing the outlets, no point in each room can be more than 3 meters away from one.
>
>**Red** represents **4** outlets, **Yellow** represents **2** outlets and **Green** represents 1 outlet.
 
![Network Outlets Deployment schematic Plan Level 2](assets/Level2.png)

**(For clarity, outlets associated with Access Points will be shown on a separate schematic)**

---

## 3. Access Points

> Both floors require LAN coverage (Wi-Fi)
> 
> Each Access Point covers a circle of 50$m$ diameter
> 
> All APs will be installed in the space above the dropped ceiling
> 
> Each AP will require **a dedicated outlet**
> 
> All APs on this terminal will operate on **5GHz band**, since this band offers a much larger number of available channels, and it also has **DFS (Dynamic Frequency Selection)**, which selects a channel in order avoid interference with its neighbours.

---
### 3.1. Calculating amount and positions

> In order to verify how many APs are needed in a certain area, it will be used the following formula:
> $$D_r = \sqrt{length^2 + width^2} \leq D_c = 2 \times radius = 50 \ m$$
> $D_r$ is the diagonal of the rectangle we are currently trying to place APs, and $D_c$ the diameter of an AP (50$m$)
> 
> If the condition is false, we will use the following formula to determine the number of APs on a certain zone (always rounded up):
> $$N = \left\lceil \frac{D_r^2}{2500} \right\rceil$$

---

#### 3.1.1. Level 0 — Rooms

| Room | $D_r = \sqrt{length^2+width^2}$ ($m$) | $D_r \leq 50m$? | Total APs |
|------|---------------------------------------|-----------------|-----------|
| 1    | √(32.8²+12.1²) = 34.91                | Yes             | **1**     |
| 2    | √(31.0²+12.1²) = 33.29                | Yes             | **1**     |
| 3    | √(25.9²+12.1²) = 28.54                | Yes             | **1**     |
| 4    | √(10.3²+12.1²) = 15.89                | Yes             | **1**     |
| 5    | √(20.7²+12.1²) = 23.95                | Yes             | **1**     |
| 6    | √(29.3²+12.1²) = 31.70                | Yes             | **1**     |
| 7    | √(25.9²+12.1²) = 28.54                | Yes             | **1**     |
| 8    | √(25.9²+12.1²) = 28.54                | Yes             | **1**     |
| 9    | √(25.9²+12.1²) = 28.54                | Yes             | **1**     |
| 10   | √(13.8²+22.4²) = 26.31                | Yes             | **1**     |
| 11a  | √(12.1²+12.1²) = 17.07                | Yes             | **1**     |
| 11b  | √(13.8²+10.3²) = 17.24                | Yes             | **1**     |
| 12   | √(25.9²+13.8²) = 29.31                | Yes             | **1**     |
| 13   | √(22.4²+13.8²) = 26.31                | Yes             | **1**     |
| 14   | √(31.0²+13.8²) = 33.96                | Yes             | **1**     |
| 15   | √(22.4²+13.8²) = 26.31                | Yes             | **1**     |
| 16   | √(22.4²+13.8²) = 26.31                | Yes             | **1**     |

**Total APs for Level 0 rooms: 17 APs + 17 Dedicated Outlets**

---

#### 3.1.2 Level 0 - Open Areas

I divided the open areas on this terminal in 6 zones (as it will be shown on the next schematic plan)

| Open Area | Dimensions ($cm$) | Length ($m$) | Width ($m$) | Area ($m^2$) | $D_r = \sqrt{L^2+W^2}$ ($m$) | $D_r \leq 50m$? | Total APs |
|-----------|-------------------|--------------|-------------|--------------|------------------------------|-----------------|-----------|
| A         | 1.1 × 0.7         | 18.97        | 12.07       | 229.0        | √(19.0²+12.1²) = 22.48       | Yes             | **1**     |
| B         | 1.6 × 5.2         | 27.59        | 89.66       | 2473.7       | √(27.6²+89.7²) = 93.81       | No              | **4**     |
| C         | 8.1 × 2.0         | 139.66       | 34.48       | 4815.5       | √(139.7²+34.5²) = 143.85     | No              | **4**     |
| D         | 1.6 × 2.6         | 27.59        | 44.83       | 1236.9       | √(27.6²+44.8²) = 52.64       | No              | **2**     |
| E         | 1.3 × 0.8         | 22.41        | 13.79       | 309.0        | √(22.4²+13.8²) = 26.31       | Yes             | **1**     |
| F         | 8.5 × 2.0         | 146.55       | 34.48       | 5053.0       | √(146.6²+34.5²) = 150.55     | No              | **5**     |

**Total APs for Level 0 open areas: 17 APs + 17 Dedicated Outlets**

**Total APs for Level 0 (rooms + open areas): 34 APs + 34 Dedicated Outlets**

---

**AP Distribution**

> **Formulas:** $R=25m$, $n_{lines} = \lceil W/(2R) \rceil$, $y_i = W(2i-1)/(2n)$, $d = \min(y_i, W-y_i)$, $c = \sqrt{R^2-d^2}$, $n_{APs} = \lfloor (L-2c)/(2c) \rfloor + 2$, spacing $= (L-2c)/(n_{APs}-1)$
>
> W - Width; L - Length; R - AP radius (25m); i - line index (1 to $n_{lines}$)
> 
> These coordinates are local to the zone itself, for future calculations, it will be used global coordinates

**Zone B** — $n_{lines}=2$, $d=22.41m$, $c=11.08m$

| AP | X ($m$) | Y ($m$) |
|----|---------|---------|
| 1  | 11.08   | 22.41   |
| 2  | 16.51   | 22.41   |
| 3  | 11.08   | 67.25   |
| 4  | 16.51   | 67.25   |

**Zone C** — $n_{lines}=1$, $d=17.24m$, $c=18.11m$

| AP | X ($m$) | Y ($m$) |
|----|---------|---------|
| 1  | 18.11   | 17.24   |
| 2  | 52.59   | 17.24   |
| 3  | 87.07   | 17.24   |
| 4  | 121.56  | 17.24   |

**Zone D** — $n_{lines}=1$, $d=22.41m$, $c=11.08m$

| AP | X ($m$) | Y ($m$) |
|----|---------|---------|
| 1  | 11.08   | 22.41   |
| 2  | 16.51   | 22.41   |

**Zone F** — $n_{lines}=1$, $d=17.24m$, $c=18.11m$

| AP | X ($m$) | Y ($m$) |
|----|---------|---------|
| 1  | 18.11   | 17.24   |
| 2  | 45.69   | 17.24   |
| 3  | 73.28   | 17.24   |
| 4  | 100.86  | 17.24   |
| 5  | 128.45  | 17.24   |

---

#### Schematic Plan (For APs and Dedicated Outlets)
>This schematic shows how to place the APs and their Dedicated Outlets.
>
> **Blue** represents an AP + Dedicated Outlet

![Access Points Schematic](assets/APsLevel0.png)

---

#### 3.2.1. Level 2 — Rooms

| Room | Area ($m^2$) | $D_r = \sqrt{L^2+W^2}$ ($m$) | $D_r \leq 50m$? | Total APs |
|------|--------------|------------------------------|-----------------|-----------|
| 1    | 395.4        | √(32.8²+12.1²) = 34.91       | Yes             | **1**     |
| 2    | 374.5        | √(31.0²+12.1²) = 33.29       | Yes             | **1**     |
| 3    | 124.8        | √(10.3²+12.1²) = 15.89       | Yes             | **1**     |
| 4    | 249.7        | √(20.7²+12.1²) = 23.95       | Yes             | **1**     |
| 5    | 312.1        | √(25.9²+12.1²) = 28.54       | Yes             | **1**     |
| 6    | 267.4        | √(25.9²+10.3²) = 27.85       | Yes             | **1**     |
| 7    | 208.1        | √(12.1²+17.2²) = 21.05       | Yes             | **1**     |
| 8    | 267.4        | √(25.9²+10.3²) = 27.85       | Yes             | **1**     |
| 9    | 208.1        | √(12.1²+17.2²) = 21.05       | Yes             | **1**     |
| 10   | 309.0        | √(13.8²+22.4²) = 26.31       | Yes             | **1**     |
| 11a  | 124.8        | √(12.1²+10.3²) = 15.89       | Yes             | **1**     |
| 11b  | 166.4        | √(13.8²+12.1²) = 18.33       | Yes             | **1**     |
| 12   | 222.9        | √(25.9²+8.6²) = 27.26        | Yes             | **1**     |
| 13   | 148.6        | √(17.2²+8.6²) = 19.27        | Yes             | **1**     |
| 14   | 178.3        | √(20.7²+8.6²) = 22.41        | Yes             | **1**     |
| 15   | 178.3        | √(20.7²+8.6²) = 22.41        | Yes             | **1**     |
| 16   | 193.2        | √(22.4²+8.6²) = 24.01        | Yes             | **1**     |
| 17   | 312.1        | √(25.9²+12.1²) = 28.54       | Yes             | **1**     |
| 18   | 270.5        | √(22.4²+12.1²) = 25.45       | Yes             | **1**     |
| 19   | 374.5        | √(31.0²+12.1²) = 33.29       | Yes             | **1**     |
| 20   | 270.5        | √(22.4²+12.1²) = 25.45       | Yes             | **1**     |
| 21   | 270.5        | √(22.4²+12.1²) = 25.45       | Yes             | **1**     |

**Total APs for Level 2 rooms: 22 APs + 22 Dedicated Outlets**

---

#### 3.2.2 Level 2 - Open Areas 
I divided the open areas on this terminal in 6 zones (as it will be shown on the next schematic plan)

| Open Area | Dimensions ($cm$) | Length ($m$) | Width ($m$) | Area ($m^2$) | $D_r = \sqrt{L^2+W^2}$ ($m$) | $D_r \leq 50m$? | Total APs |
|-----------|-------------------|--------------|-------------|--------------|------------------------------|-----------------|-----------|
| A         | 3.1 × 0.7         | 53.45        | 12.07       | 645.1        | √(53.5²+12.1²) = 54.80       | No              | **2**     |
| B         | 7.3 × 1.5         | 125.86       | 25.86       | 3254.7       | √(125.9²+25.9²) = 128.49     | No              | **3**     |
| C         | 0.7 × 1.9         | 12.07        | 32.76       | 395.4        | √(12.1²+32.8²) = 34.91       | Yes             | **1**     |
| D         | 1.3 × 1.2         | 22.41        | 20.69       | 463.7        | √(22.4²+20.7²) = 30.50       | Yes             | **1**     |
| E         | 10.1 × 2.6        | 174.14       | 44.83       | 7806.7       | √(174.1²+44.8²) = 179.82     | No              | **8**     |
| F         | 1.7 × 5.9         | 29.31        | 101.72      | 2981.4       | √(29.3²+101.7²) = 105.86     | No              | **3**     |

**Total APs for Level 2 open areas: 18 APs+ 18 Dedicated Outlets**

**Total APs for Level 2 (rooms + open areas): 40 APs + 40 Dedicated Outlets**

---

**AP Distribution**

>Same method as the other Level

**Zone A** — $n_{lines}=1$, $d=6.04m$, $c=24.26m$

| AP | X ($m$) | Y ($m$) |
|----|---------|---------|
| 1  | 24.26   | 6.04    |
| 2  | 29.19   | 6.04    |

**Zone B** — $n_{lines}=1$, $d=12.93m$, $c=21.40m$

| AP | X ($m$) | Y ($m$) |
|----|---------|---------|
| 1  | 21.40   | 12.93   |
| 2  | 62.93   | 12.93   |
| 3  | 104.46  | 12.93   |

**Zone E** — $n_{lines}=1$, $d=22.41m$, $c=11.07m$

| AP | X ($m$) | Y ($m$) |
|----|---------|---------|
| 1  | 11.08   | 22.41   |
| 2  | 32.79   | 22.41   |
| 3  | 54.50   | 22.41   |
| 4  | 76.21   | 22.41   |
| 5  | 97.93   | 22.41   |
| 6  | 119.64  | 22.41   |
| 7  | 141.35  | 22.41   |
| 8  | 163.06  | 22.41   |

**Zone F** — $n_{lines}=3$, zone too narrow ($L < 2c$); 1 AP per line at $x=L/2=14.65m$

| AP | X ($m$) | Y ($m$) |
|----|---------|---------|
| 1  | 14.65   | 16.95   |
| 2  | 14.65   | 50.86   |
| 3  | 14.65   | 84.77   |


---

#### Schematic Plan (For APs and Dedicated Outlets)
>This schematic shows how to place the APs and their Dedicated Outlets.
>
> **Blue** represents an AP + Dedicated Outlet

![Access Points Schematic](assets/APsLevel2.png)

---

## 4. Cross Connections
 
>Each cable (whatever their type is) length should be less than 90$m$
> 
>Straight line distance between the horizontal cross-connect should be less than 80 meters
> 
>Cables connecting an IC to a HC are limited to 500 meters long
> 
>Cables connecting an MC to an IC are limited to 1500 meters long
> 
>Each enclosure has a size of 42U, which means, it fits 200 connections (1U must be free)
>
>There needs to be one IC per level
> 
>All HCs will be placed on the dropped ceiling 

---

### 4.1. Positioning of HCs 

HCs will be positioned in places where they can serve the biggest amount of rooms/open areas as possible. To verify the straight distance between an outlet and a HC, it will be used:

$$d = \sqrt{(cx_{room} - x_{HC})^2 + (cy_{room} - y_{HC})^2}$$

On **Level 0**, we will place **5 HCs**

On **Level 2**, we will place **6 HCs**

Since CPs (Consolidation Points) adds an extra connection point in horizontal cable pathways, and since it increases the chances of a potential point of failure (making it harder to understand where the fault is), HCs will be placed in a way where CPs won't be needed.

The **X** coordinate of an HC will be chosen based on the rooms they will serve, while the **Y** coordinate will be chosen based on the midpoint between 2 rooms heights, or chosen in a way that reduces cable length.

---

### 4.2. Level 0 - HCs positions and rooms/areas assigned

The IC will be placed within the Room 4, in this case, I considered X = 118 & Y = 3, since it makes the IC being close to the vertical passageway
The MC will be co-located with this IC.

| HC      | X ($m$) | Y ($m$) | Rooms served                     | Outlets | APs | APs served                 | Total   |
|---------|---------|---------|----------------------------------|---------|-----|----------------------------|---------|
| HC-L0-1 | 37      | 41      | R1, R8, R9, R10, R11a, R11b, R12 | 152     | 13  | 7 room APs + zones B, D    | **165** |
| HC-L0-2 | 62      | 41      | R2, R3                           | 140     | 4   | 2 room APs + zones C, F    | **144** |
| HC-L0-3 | 83      | 41      | R4, R13, R14                     | 148     | 7   | 3 room APs + zones A, C, F | **155** |
| HC-L0-4 | 136     | 41      | R5, R6, R15                      | 184     | 7   | 3 room APs + zones C, E, F | **191** |
| HC-L0-5 | 175     | 41      | R7, R16                          | 126     | 3   | 2 room APs + zone F        | **129** |

**Total: 5 HCs**

---

#### 4.2.1. Level 0 - Cable Distance Validation

All distances will be measured on a straight-line from HC to the room center or the AP position. If $d > 90m$, a CP is required.

**HC-L0-1** 

| Connection | Coordinates    | Distance |
|------------|----------------|----------|
| R1         | (16.38, 6.04)  | 40.5$m$  |
| R8         | (6.04, 18.11)  | 38.6$m$  |
| R9         | (6.04, 29.31)  | 33.1$m$  |
| R10        | (6.89, 68.11)  | 40.5$m$  |
| R11a       | (19.82, 62.94) | 27.8$m$  |
| R11b       | (20.68, 74.14) | 36.9$m$  |
| R12        | (40.52, 75.86) | 35$m$    |
| B-AP1      | (11.08, 32.41) | 27.3$m$  |
| B-AP2      | (16.51, 32.41) | 22.2$m$  |
| B-AP3      | (11.08, 77.25) | 44.4$m$  |
| B-AP4      | (16.51, 77.25) | 41.6$m$  |
| D-AP1      | (11.08, 56.89) | 30.4$m$  |
| D-AP2      | (16.51, 56.89) | 25.9$m$  |

**HC-L0-2**

| Connection | Coordinates    | Distance |
|------------|----------------|----------|
| R2         | (48.27, 6.04)  | 37.6$m$  |
| R3         | (76.72, 6.04)  | 37.9$m$  |
| C-AP1      | (45.70, 17.24) | 28.8$m$  |
| F-AP1      | (45.70, 72.24) | 35.2$m$  |

**HC-L0-3**

| Connection | Coordinates     | Distance |
|------------|-----------------|----------|
| R4         | (108.62, 6.04)  | 43.3$m$  |
| R13        | (64.66, 75.86)  | 39.4$m$  |
| R14        | (91.38, 75.86)  | 35.9$m$  |
| A-AP1      | (94.48, 6.04)   | 36.8$m$  |
| C-AP2      | (80.18, 17.24)  | 23.9$m$  |
| F-AP2      | (73.28, 72.24)  | 32.7$m$  |
| F-AP3      | (100.87, 72.24) | 36$m$    |

**HC-L0-4** 

| Connection | Coordinates     | Distance |
|------------|-----------------|----------|
| R5         | (124.14, 6.04)  | 36.9$m$  |
| R6         | (149.13, 6.04)  | 37.3$m$  |
| R15        | (118.11, 75.86) | 39.2$m$  |
| C-AP3      | (114.66, 17.24) | 31.9$m$  |
| C-AP4      | (149.15, 17.24) | 27.2$m$  |
| E-AP1      | (140.52, 61.89) | 21.4$m$  |
| F-AP4      | (128.45, 72.24) | 32.1$m$  |

**HC-L0-5** 

| Connection | Coordinates     | Distance |
|------------|-----------------|----------|
| R7         | (176.72, 6.04)  | 35$m$    |
| R16        | (175, 75.86)    | 34.9$m$  |
| F-AP5      | (156.04, 72.24) | 36.5$m$  |

---
#### Schematic Plan (Cross Connections)
>This schematic shows how to place MC, IC and HCs on Level 0
>
> **Red** represents the MC, **Blue** the IC and **Green** a HC

![Cross Connections Schematic](assets/HCsLevel0.png)

---


### 4.3. Level 2 - HCs positions and rooms/areas assigned

The IC will be placed within the Room 3, in this case, I considered X = 118 & Y = 3, since it makes the IC being close to the vertical passageway

| HC      | X ($m$) | Y ($m$) | Rooms served                          | Outlets | APs | APs served                    | Outlets (External Walls) | Total   |
|---------|---------|---------|---------------------------------------|---------|-----|-------------------------------|--------------------------|---------|
| HC-L2-1 | 30      | 20      | R1, R6, R8, R10, R11a, R11b, R12, R17 | 190     | 8   | 8 room APs                    | 0                        | **198** |
| HC-L2-2 | 55      | 57      | R2, R13, R18                          | 162     | 7   | 3 room APs + zone E           | 19                       | **188** |
| HC-L2-3 | 91      | 41      | R3, R14, R19                          | 112     | 7   | 3 room APs + zones A, B, E    | 2                        | **121** |
| HC-L2-4 | 122     | 41      | R4, R15, R16, R20                     | 182     | 7   | 4 room APs + zones B, E       | 9                        | **198** |
| HC-L2-5 | 161     | 35      | R5, R21                               | 120     | 3   | 2 room APs + zone B           | 1                        | **124** |
| HC-L2-6 | 183     | 41      | R7, R9                                | 84      | 8   | 2 room APs + zones C, D, E, F | 28                       | **120** |

**Total: 6 HCs**

---

#### 4.3.1. Level 2 - Cable Distance Validation

**HC-L2-1** 

| Connection | Coordinates    | Distance |
|------------|----------------|----------|
| R1         | (16.38, 6.04)  | 19.5$m$  |
| R6         | (12.93, 17.24) | 17.3$m$  |
| R8         | (12.93, 27.58) | 18.7$m$  |
| R10        | (6.89, 66.38)  | 51.8$m$  |
| R11a       | (19.82, 60.34) | 41.6$m$  |
| R11b       | (20.68, 71.55) | 52.4$m$  |
| R12        | (40.52, 52.59) | 34.2$m$  |
| R17        | (40.52, 62.94) | 44.2$m$  |

**HC-L2-2** 

| Connection          | Coordinates                                           | Distance |
|---------------------|-------------------------------------------------------|----------|
| R2                  | (48.27, 6.04)                                         | 51.4$m$  |
| R13                 | (62.07, 52.59)                                        | 8.3$m$   |
| R18                 | (68.97, 62.94)                                        | 15.2$m$  |
| E-AP1               | (11.08, 91.38)                                        | 55.8$m$  |
| E-AP2               | (32.79, 91.38)                                        | 40.9$m$  |
| E-AP3               | (54.50, 91.38)                                        | 34.4$m$  |
| E-AP4               | (76.21, 91.38)                                        | 40.4$m$  |
| External Walls (19) | Max distance at (5, 100) using Pathway at (0.9, 99.4) | 78.4$m$  |

**HC-L2-3**

| Connection         | Coordinates                                               | Distance |
|--------------------|-----------------------------------------------------------|----------|
| R3                 | (108.62, 6.04)                                            | 39.1$m$  |
| R14                | (86.20, 52.59)                                            | 12.5$m$  |
| R19                | (100, 62.94)                                              | 23.7$m$  |
| A-AP1              | (88.05, 6.04)                                             | 35.1$m$  |
| A-AP2              | (92.98, 6.04)                                             | 35$m$    |
| B-AP1              | (85.19, 25)                                               | 17$m$    |
| E-AP5              | (97.93, 91.38)                                            | 50.9$m$  |
| External Walls (2) | Max distance at (100, 100) using Pathway at (101.1, 99.4) | 63.8$m$  |

**HC-L2-4** 

| Connection         | Coordinates                                               | Distance |
|--------------------|-----------------------------------------------------------|----------|
| R4                 | (124.14, 6.04)                                            | 35$m$    |
| R15                | (106.89, 52.59)                                           | 19$m$    |
| R16                | (128.44, 52.59)                                           | 13.3$m$  |
| R20                | (126.72, 62.94)                                           | 22.4$m$  |
| B-AP2              | (126.72, 25)                                              | 16.7$m$  |
| E-AP6              | (119.64, 91.38)                                           | 50.4$m$  |
| E-AP7              | (141.35, 91.38)                                           | 54$m$    |
| External Walls (9) | Max distance at (145, 100) using Pathway at (151.5, 99.4) | 77.5$m$  |

**HC-L2-5**

| Connection        | Coordinates                               | Distance |
|-------------------|-------------------------------------------|----------|
| R5                | (161.20, 6.04)                            | 29$m$    |
| R21               | (166.38, 59.48)                           | 25.1$m$  |
| B-AP3             | (168.25, 25)                              | 12.4$m$  |
| External Wall (1) | (155, 100) using Pathway at (151.5, 99.4) | 69.2$m$  |

**HC-L2-6** 

| Connection          | Coordinates                                               | Distance |
|---------------------|-----------------------------------------------------------|----------|
| R7                  | (178.44, 20.69)                                           | 20.8$m$  |
| R9                  | (178.44, 43.10)                                           | 5$m$     |
| C-AP1               | (195.69, 16.38)                                           | 27.7$m$  |
| D-AP1               | (175, 44.82)                                              | 8.9$m$   |
| E-AP8               | (163.06, 91.38)                                           | 54.2$m$  |
| F-AP1               | (204.30, 16.95)                                           | 32.1$m$  |
| F-AP2               | (204.30, 50.86)                                           | 23.5$m$  |
| F-AP3               | (204.30, 84.77)                                           | 48.7$m$  |
| External Walls (28) | Max distance at (160, 100) using Pathway at (151.5, 99.4) | 75.5$m$  |

---
#### Schematic Plan (Cross Connections)
>This schematic shows how to place HCs and IC on Level 2
>
> **Blue** represents the IC and **Green** a HC

![Cross Connections Schematic](assets/HCsLevel2.png)

---

## 5. Cable Pathways

> The cable length is calculated by using the straight line between the HC and the room/area it serves.
> 
> **MC → IC:** The MC will connect to the IC on both levels.
> 
> **IC → HC:** The IC will connect to all HCs on their specific level, using the dropped ceiling.
> 
> **Room outlets:** $d_{HC \to room\_center} \times N_{outlets}$ — in order to simply calculations
>
> **APs (room or open area):** $d_{HC \to AP\_position}$ - since each AP has a dedicated outlet
> 
> **External wall outlets (Level 2):** cables run from the HC horizontally through the dropped ceiling, until the nearest underfloor raceway access point on the external wall, then along the underfloor cable pathway to the outlet position. Cable length = $d_{HC \to access\ point} + d_{raceway\ to\ outlet}$
> 
> **Cable Redundancy** will be considered to connect **MC → IC** and **IC → HC** 

---

### 5.1. MC → IC

The MC and the IC on Level 0 will be co-located, since both will be on Room 4. We will consider 1$m$ of cable for this connection.
To connect the MC to the IC on Level 2, we will need to use the vertical passageway to go up 9$m$.

**Total cable length for MC → IC connections: 10$m$**

**Total cable length for MC → IC connections (with cable redundancy): 20$m$**

---

### 5.2. IC → HC

Since there are 2 ICs, one on each floor, we only need 

| Connection    | Distance |
|---------------|----------|
| IC0 → HC-L0-1 | 89.5$m$  |
| IC0 → HC-L0-2 | 67.7$m$  |
| IC0 → HC-L0-3 | 51.7$m$  |
| IC0 → HC-L0-4 | 42.1$m$  |
| IC0 → HC-L0-5 | 68.5$m$  |
| IC2 → HC-L2-1 | 89.6$m$  |
| IC2 → HC-L2-2 | 82.9$m$  |
| IC2 → HC-L2-3 | 46.5$m$  |
| IC2 → HC-L2-4 | 38.2$m$  |
| IC2 → HC-L2-5 | 53.6$m$  |
| IC2 → HC-L2-6 | 75.3$m$  |

**Total cable length for IC → HC connections : 705,6$m$**

**Total cable length for IC → HC connections (with cable redundancy) : 1411,2$m$**

---

### 5.3 HCs - Outlets (Level 0)

| HC                | Type                                                     | Cables  | Total Cable length |
|-------------------|----------------------------------------------------------|---------|--------------------|
| HC-L0-1           | Room outlets (R1: 40.5m×80, R12: 35.0m×72)               | 152     | 5760$m$            |
| HC-L0-1           | APs — 13 cables                                          | 13      | 445$m$             |
| **HC-L0-1 Total** | -                                                        | **165** | **6213$m$**        |
| HC-L0-2           | Room outlets (R2: 37.6m×76, R3: 37.9m×64)                | 140     | 5282$m$            |
| HC-L0-2           | APs — 4 cables                                           | 4       | 140$m$             |
| **HC-L0-2 Total** | -                                                        | **144** | **5422$m$**        |
| HC-L0-3           | Room outlets (R13: 39.4m×62, R14: 35.9m×86)              | 148     | 5526$m$            |
| HC-L0-3           | APs — 7 cables                                           | 7       | 248$m$             |
| **HC-L0-3 Total** | -                                                        | **155** | **5774$m$**        |
| HC-L0-4           | Room outlets (R5: 36.9m×50, R6: 37.3m×72, R15: 39.2m×62) | 184     | 6964$m$            |
| HC-L0-4           | APs — 7 cables                                           | 7       | 226$m$             |
| **HC-L0-4 Total** | -                                                        | **191** | **7190$m$**        |
| HC-L0-5           | Room outlets (R7: 35.0m×64, R16: 34.9m×62)               | 126     | 4401$m$            |
| HC-L0-5           | APs — 3 cables                                           | 3       | 106$m$             |
| **HC-L0-5 Total** | -                                                        | **129** | **4508$m$**        |
| **Level 0 Total** | -                                                        | **784** | **29107$m$**       |

---

### 5.4. Horizontal copper — Level 2

| HC                | Type                                                                             | Cables  | Total Cable length |
|-------------------|----------------------------------------------------------------------------------|---------|--------------------|
| HC-L2-1           | Room outlets (R1: 19.5$m$×80, R12: 34.2$m$×46, R17: 44.2$m$×64)                  | 190     | 5962$m$            |
| HC-L2-1           | APs — 8 cables                                                                   | 8       | 280$m$             |
| **HC-L2-1 Total** | -                                                                                | **198** | **6242$m$**        |
| HC-L2-2           | Room outlets (R2: 51.4$m$×76, R13: 8.3$m$×30, R18: 15.2$m$×56)                   | 162     | 5007$m$            |
| HC-L2-2           | APs — 7 cables                                                                   | 7       | 246$m$             |
| HC-L2-2           | External wall outlets — 19 cables (Max: 78)                                      | 19      | 1490$m$            |
| **HC-L2-2 Total** | -                                                                                | **188** | **6743$m$**        |
| HC-L2-3           | Room outlets (R14: 12.5$m$×36, R19: 23.74$m$×76)                                 | 112     | 2254$m$            |
| HC-L2-3           | APs — 7 cables                                                                   | 7       | 213$m$             |
| HC-L2-3           | External wall outlets — 2 cables (Max: 64$m$)                                    | 2       | 128$m$             |
| **HC-L2-3 Total** | -                                                                                | **121** | **2595$m$**        |
| HC-L2-4           | Room outlets (R4: 35.0$m$×50, R15: 19.0$m$×36, R16: 13.3$m$×40, R20: 22.4$m$×56) | 182     | 4224$m$            |
| HC-L2-4           | APs — 7 cables                                                                   | 7       | 211$m$             |
| HC-L2-4           | External wall outlets — 9 cables (Max: 78$m$)                                    | 9       | 698$m$             |
| **HC-L2-4 Total** | -                                                                                | **198** | **5133$m$**        |
| HC-L2-5           | Room outlets (R5: 29.0$m$×64, R21: 25.1$m$×56)                                   | 120     | 3257$m$            |
| HC-L2-5           | APs — 3 cables                                                                   | 3       | 66$m$              |
| HC-L2-5           | External wall outlets — 1 cable (Max: 69$m$)                                     | 1       | 69$m$              |
| **HC-L2-5 Total** | -                                                                                | **124** | **3392$m$**        |
| HC-L2-6           | Room outlets (R7: 20.8$m$×42, R9: 5.0$m$×42)                                     | 84      | 1085$m$            |
| HC-L2-6           | APs — 8 cables                                                                   | 8       | 221$m$             |
| HC-L2-6           | External wall outlets — 28 cables (Max: 76$m$)                                   | 28      | 2114$m$            |
| **HC-L2-6 Total** | -                                                                                | **120** | **3420$m$**        |
| **Level 2 Total** | -                                                                                | **949** | **27526$m$**       |
