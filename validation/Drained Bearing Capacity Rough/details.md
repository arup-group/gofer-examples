# Central St Giles: Flexible cantilever retaining wall validation

![csg-photo](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/csg-hufton-crow.png)

Central St Giles, Bloomsbury, &copy; Hufton Crow.

## Summary

Completed in 2010, Arup provided engineering consultancy services for the redevelopment of Central St Giles, London, as a mixed-use multi-storey development. **Oasys Frew** was used to design the flexible cantilever retaining walls forming the new basement.

For this example, we have compared Gofer and Frew, using the Central St Giles design models.

![3d-model](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/csg-arup-3d-model.png)

*Artist's impression of the site, Robert Powell &copy; Arup*

### The site

Central St Giles is located east of Tottenham Court Road, south of New Oxford Street, close to Tottenham Court Road underground station. The site was previously occupied by a 1950s office building, and Victorian and Georgian residential buildings.

#### Site obstructions

- **Historic** basements and foundations

- Major **utility statutory services** (including water mains, 3-phase cables, and a basement-level electrical substation)

- A section overlapping with the **Crossrail** route

![map](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/site-boundary.png)

*Proposed site boundary, adjacent to the Crossrail tunnel exclusion zone.*

## Model inputs

### Ground conditions

A 2006 ground investigation\* revealed a downward geological sequence comprising: **Made Ground, River Terrace Deposits, London Clay, Lambeth Group, Thanet Sands** and **Chalk**.

**_Table 1: Generic ground model across the site_**

| Stratum    | Elevation |
| ---------- | --------- |
| [-]        | [m_OD]    |
| MG         | 24.0      |
| RTD        | 20.0      |
| LC         | 17.0      |
| LMG        | -3.5      |
| Model base | -21.0     |

_*2006 ground investigation, supplemented by results from Crossrail / King’s Cross developments._

## Parameters

The following parameters were used when modelling the flexible retaining wall.

**_Table 2: Ground model parameters_**

| Stratum | $\gamma$           | $\upsilon$ | $\upsilon$' | $C_{u\theta}$       | $E_{u\theta}$              | $E_{\theta}$'             | $\phi$       | $K_{0}$ | $K_{r}$ |
| ------- | ------------------ | ---------- | ----------- | ------------------- | -------------------------- | ------------------------- | ------------ | ------- | ------- |
| [-]     | [kN/m<sup>3</sup>] | [-]        | [-]         | [kPa]               | [kPa]                      | [kPa]                     | $[\degree ]$ | [-]     | [-]     |
| MG      | 18                 | -          | 0.3         | -                   | -                          | 75,000                    | 25           | 0.577   | 0.429   |
| RTD     | 20                 | -          | 0.3         | -                   | -                          | 50,000                    | 36           | 0.412   | 0.429   |
| LC      | 20                 | 0.5        | 0.2         | 90 + 7.1 $\times$ z | 67,500 + 5,325 $\times$ z  | 56,250 + 4,438 $\times$ z | 25           | 1       | 1       |
| LMG     | 20                 | 0.5        | 0.2         | 258 + 8 $\times$ z  | 128,800 + 3,200 $\times$ z | 77,400 + 2,400 $\times$ z | 26           | 1       | 1       |

*N.B.: \***z** is the datum (0 m) that refers to the top elevation of the relevant layer (see Table 1). Gradient is taken in kPa/m below z reference value.*

## Structure modelling

The proposed design secant wall was composed by **1,180mm diameter piles** with **980mm centres**. Casing was **+15.0mOD**, with **1,050mm diameter piles** below the casing. In both Gofer and Frew we used an equivalent **1,030mm** section with the following parameters:

**_Table 3: STR parameters for a flexible retaining wall with steel piles_**

| Width | Depth | i               | E<sub>steel</sub> | Area             | $EA$       | $EI$               |
| ----- | ----- | --------------- | ----------------- | ---------------- | ---------- | ------------------ |
| [m]   | [m]   | [m<sup>4</sup>] | [kPa]             | [m]<sup>2</sup>] | [kN]       | [kN*m<sup>4</sup>] |
| 1.03  | 1.00  | 0.091061        | 40,000,000        | 1.03             | 41,200,000 | 3,642,423.3        |

### Loading conditions

Design loading information was provided and implemented as follows:

- Berm surcharge on retained side: **14.4kPa**

### Construction sequence

The following construction stages were recreated within Gofer and Frew, to represent the actual construction sequence:

- Initialisation

- Wall installation (and apply berm surcharge)

- Excavation (MG, 4m bgl)

- Excavation (RTD, 7m bgl) to formation

### Modelling assumptions

- For simplicity we have assumed full friction between the soil and structures modelled

- Porewater pressure (PWP): Hydrostatic only (no flow)

- Excess PWP not calculated. No consolidation

- Total stress approach used, with undrained parameters switched once from drained to undrained

## How they compare

### Display

Ground conditions as displayed in Gofer (left) and Frew (right).

| Gofer | Frew |
|-------- |------- |
| ![gofer-model](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/goferlast-stage.png) | ![frew-model](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/frew-last-stage.png) |

### Results

For displacements, bending moments and shear forces, Frew results tend to be slightly higher or lower, but are considered comparable. Further subdivisions of the LC material parameters, particularly stiffness, have minimal impact on the results.

Both models give similar results for the maximum bending moment, which is reflected in the design of this type of structure.

| Displacement | Bending moment | Shear forces |
|-------- |------- | ------- |
| ![displacement-graph](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/displacement-graph.png)   | ![bending-moment-graph](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/bending-moment-graph.png)  | ![shear-forces-graph](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/shear-forces-graph.png) |

**References:**

Chris Barker, Marek Niewiarowski and Dinesh Patel (Arup London, UK, 2010). [\*Central Saint Giles – Basement And Foundations Designed For Future Crossrail Tunnelling.](https://www.researchgate.net/publication/361616899_CENTRAL_SAINT_GILES_-BASEMENT_AND_FOUNDATIONS_DESIGNED_FOR_FUTURE_CROSSRAIL_TUNNELLING)\*
