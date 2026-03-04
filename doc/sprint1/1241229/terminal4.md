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
> Rooms **without** outlets : 4 (HC), 8, 9, 10, 11

---

#### 2.1.1. Room Areas & Outlet Calculation

| Room | Dimensions ($cm$) | Length ($m$) | Width ($m$) | Area ($m^2$) | (Area / 10) (rounded up) | Outlets (x2) | 
|------|-------------------|--------------|-------------|--------------|--------------------------|--------------|
| 1    | 1.9 × 0.7         | 32.76        | 12.07       | 395.4        | 40                       | **80**       | 
| 2    | 1.8 × 0.7         | 31.03        | 12.07       | 374.9        | 38                       | **76**       |
| 3    | 1.5 × 0.7         | 25.86        | 12.07       | 312.4        | 32                       | **64**       |
| 5    | 1.2 × 0.7         | 20.69        | 12.07       | 249.7        | 25                       | **50**       |
| 6    | 1.7 × 0.7         | 29.31        | 12.07       | 354.0        | 36                       | **72**       |
| 7    | 1.5 × 0.7         | 25.86        | 12.07       | 312.4        | 32                       | **64**       |
| 12   | 1.5 × 0.8         | 25.86        | 13.79       | 356.6        | 36                       | **72**       |
| 13   | 1.3 × 0.8         | 22.41        | 13.79       | 308.8        | 31                       | **62**       |
| 14   | 1.8 × 0.8         | 31.03        | 13.79       | 427.9        | 43                       | **86**       |
| 15   | 1.3 × 0.8         | 22.41        | 13.79       | 308.8        | 31                       | **62**       | 
| 16   | 1.3 × 0.8         | 22.41        | 13.79       | 308.8        | 31                       | **62**       |

**Total standard outlets for Level 0: 750**

---

#### Schematic Plan (For Standard Outlets Only)
>This schematic shows an example layout for the outlets on the Level. The plan **is not** drawn to scale, as doing so would make the diagram too difficult to read. 
>
>When placing the outlets, no point in each room can be more than 3 meters away from one. 

![Network Outlets Deployment schematic Plan Level 0](assets/EsquemaOutletsLevel0.jpg)
**(For clarity, outlets associated with Access Points will be shown on a separate schematic)**

---

### 2.2. Level 2 (Departures)


> Rooms **with** standard outlets: 1, 2, 4, 5, 7, 9, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21
> 
> Rooms **without** outlets: 3 (HC — network infrastructure), 6, 8, 10, 11

---

#### 2.2.1. Room Areas & Outlet Calculation

| Room | Dimensions ($cm$) | Length ($m$) | Width ($m$) | Area ($m^2$) | (Area / 10) (rounded up) | Outlets (x2) |
|------|-------------------|--------------|-------------|--------------|--------------------------|--------------|
| 1    | 1.9 × 0.7         | 32.76        | 12.07       | 395.4        | 40                       | **80**       |
| 2    | 1.8 × 0.7         | 31.03        | 12.07       | 374.9        | 38                       | **76**       |
| 4    | 1.2 × 0.7         | 20.69        | 12.07       | 249.7        | 25                       | **50**       |
| 5    | 1.5 × 0.7         | 25.86        | 12.07       | 312.4        | 32                       | **64**       |
| 7    | 0.7 × 1.0         | 12.07        | 17.24       | 208.0        | 21                       | **42**       |
| 9    | 0.7 × 1.0         | 12.07        | 17.24       | 208.0        | 21                       | **42**       |
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

| Wall   | Real Length ($m$) | Outlets (length / 5) |
|--------|-------------------|----------------------|
| Right  | 100               | **20**               |
| Bottom | 200               | **40**               |

**Total standard outlets for external walls on Level 2: 60**

**Total standard outlets for Level 2: 910**

---

#### Schematic Plan (For Standard Outlets Only)
>This schematic shows an example layout for the outlets on the Level. The plan **is not** drawn to scale, as doing so would make the diagram too difficult to read.
>
>When placing the outlets, no point in each room can be more than 3 meters away from one.

![Network Outlets Deployment schematic Plan Level 2](assets/EsquemaOutletsLevel2.jpg)
**(For clarity, outlets associated with Access Points will be shown on a separate schematic)**

---

## 3. Access Points

>Both floors require LAN coverage (Wi-Fi)
> 
> Each Access Point covers a circle of 50$m$ diameter
> 
> All APs will be installed in the space above the dropped ceiling
> 
> Each AP will require **a dedicated outlet**

---

### 3.1. Calculating amount and positions
- Length (200m): 200 / 50 = **4 APs + 4 Outlets**
- Width (100m): 100 / 50 = **2 APs + 2 Outlets**
- **Total per level: 4 × 2 = 8 APs + 8 Outlets**
- **Total on both levels: 8 × 2 = 16 APs + 16 Outlets**
> X = 0 on the left wall; Y = 0 on the upper wall

| AP  | X ($m$) | Y ($m$) |
|-----|---------|---------|
| AP1 | 25      | 25      |
| AP2 | 25      | 75      |
| AP3 | 75      | 25      |
| AP4 | 75      | 75      |
| AP5 | 125     | 25      |
| AP6 | 125     | 75      |
| AP7 | 175     | 25      |
| AP8 | 175     | 75      |

---

#### Schematic Plan (For APs and Dedicated Outlets)
>This schematic shows how to place the APs and their Dedicated Outlets. Because each level requires 8 APs in the exact same positions, this schematic applies to all levels.

![Access Points Schematic](assets/EsquemaAPLevel0&2.jpg)

---

## 4. HC and CP






