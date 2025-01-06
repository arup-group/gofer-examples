## Gravity retaining wall

### Summary

We used Gofer to calculate the existing factor of safety (FoS) of a gravity retaining wall. A new structure was then modelled behind the gravity wall and the impact on the wall was assessed. In both situations we compared our results to equivalent Plaxis 2D models.

A summary of the geometry and key parameters is presented below.

### Modelling process

Gofer can be used to model and assess the stability of a gravity retaining wall. We modelled the existing gravity retaining wall to get the existing FoS (Model 1) and then used the second model to understand how it would be impacted by a new structure (in Model 2). The results can be visually compared. 

#### Model 1: Initial conditions

The initial model simulated a gravity retaining wall and included graded backfill in its geometry.

![Model 1 with existing gravity wall](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/geometry_modelled_wall-with-graded-backfill.png)

As you can see in the image above:
- The mesh was refined locally to the wall in expected areas of high stress and strain gradient. We did this by adjusting the local element size at the appropriate model vertices to 0.1m. The remaining vertices were left at the automatic mesh size.

- A 10kPa surface load as applied behind the retaining wall, extending to the back of the stem. Over the width of the L wall base and above the retaining wall, the load was linearly reduced in magnitude from 10kPa to 0kPa. 
-  Groundwater is modelled at the underside of the wall.

- An interface was modelled along the underside of the L section wall, with a dummy plate.

#### Model 2: Impact of new construction behind the wall

After copying the initial model in Gofer, we were ready to proceed to refining the conditions with the inclusion of a new construction behind the wall. This we represented as a buried structural element and a 100kPa applied load as follows: 

![Model 2 with new construction behind existing gravity wall](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/new-construction-wall-refined-model.png)

We included Interfaces along this structure. We opted to keep it simple in this case, modelling only the foundation and retaining the pre-existing surface load.

### Parameters used

#### Soil parameters

| | Foundation sand | Backfill |	L section wall |
|---|---|---|---|
| Constitutive model |	Mohr-Coulomb drained |	Mohr-Coulomb drained |	Linear elastic drained |
| Unit weight |	19 kN/m³ |	20 kN/m³ |	24 kN/m³ |
| Initial k0	| 0.5 |	0.5 |	1 |
| Young’s modulus |	15 MPa + 1 MPa/m below 10m |	50 MPa | 28 GPa |
| Poisson’s ratio	| 0.15 |	0.2 |	0.2 |
| Friction angle |	33º |	38º |	n/a |
| Interface reduction factor |	0.67 |	0.67 |	n/a |

#### Structural parameters

| | Dummy structure beneath L section wall |	New structure behind wall |
|---|---|---|
| Density |	0.1 kN/m³ |	0.1 kN/m³ |
| Thickness |	0.1 m |	1 m |
| Young’s modulus |	28 GPa |	28 GPa |
| Poisson’s ratio |	0.2 |	0.2 |

### Construction sequence

We assumed the following construction sequence:

<div class="begin-examples"></div>

#### Existing conditions
1.	Initialisation
2.	Build gravity wall
3.	Backfill behind the wall

Apply 10kPa load behind the wall

4.	Calculate existing FoS	
<div class="end-examples"></div>

<div class="begin-examples"></div>

#### New construction
1.	Initialisation
2.	Build gravity wall
3.	Backfill behind the wall

Apply 10kPa load behind the wall

4.	Build the new structure behind the wall
5.	Apply the new 100kPa loading behind the wall
6.	Calculate new FoS

<div class="end-examples"></div>

### Output and comparison to Plaxis

| | Gofer	| Plaxis |
|---|---|---|
| Existing gravity wall FoS | 1.54 ![Gofer results with existing gravity wall FoS](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/Gofer_existing-gravity-wall-FoS.png)| 1.55  ![Plaxis results with existing gravity wall FoS](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/Plaxis_existing-gravity-wall-FoS.png)|
| Resultant movement vector of wall from new construction | 24 to 27mm | 25 to 33 mm |
| Lateral sliding of wall base from new construction | 17mm | 21 mm |
| New gravity wall FoS | 1.22 ![gofer-slope](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/Gofer_new-gravity-wall-FoS.png)| 1.20 ![gofer-slope](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/Plaxis_new-gravity-wall-FoS.png)|

We used Gofer to assess the existing stability of a gravity L section retaining wall. We then proceeded to assess the impact on that wall of a proposed construction behind it, both in terms of displacements and reduction in factor of safety. The results compare well to an equivalent analysis done using Plaxis 2D v2024.

Gofer’s analysis delivered values consistent with similar conditions in Plaxis in the existing stability, FoS reduction and displacements. As you can see in the figures above, the computed solutions in Gofer delivered results that compare favourably with a similar model in Plaxis.