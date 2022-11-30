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

![soil-layers](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/soil-layers-table.png)

_*2006 ground investigation, supplemented by results from Crossrail / King’s Cross developments._

## Parameters

The following parameters were used when modelling the flexible retaining wall.

**_Table 2: Ground model parameters_**

![ground-model-parameters](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/stratum-table.png)

*N.B.: \***z** is the datum (0 m) that refers to the top elevation of the relevant layer (see Table 1). Gradient is taken in kPa/m below z reference value.*

## Structure modelling

The proposed design secant wall was composed by **1,180mm diameter piles** with **980mm centres**. Casing was **+15.0mOD**, with **1,050mm diameter piles** below the casing. In both Gofer and Frew we used an equivalent **1,030mm** section with the following parameters:

**_Table 3: STR parameters for a flexible retaining wall with steel piles_**

![width-depth](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/width-depth-table.png)

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
