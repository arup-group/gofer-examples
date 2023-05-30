# Steady state seepage validation part 4: Dewatering Pit 

## Summary

This model demonstrates the seepage analysis functionality of modelling within Gofer. We have used a simplified example of an issue frequently encountered by engineers analysing temporary works, linked to excavations under the phreatic level.

As with Part 3, we tested Gofer’s **steady state seepage (SSS)** features by modelling a homogeneous single layer medium, with isotropic materials for both the soil and the cut-off walls on both sides of the excavation. The boundary conditions include hydraulic head and infiltration rate on the top left model surface. 

This example is used to validate a comparison of results from **Gofer, Oasys Slope**, **Plaxis and SEEP/W**. 

## Background

Dewatering of excavations, e.g., during basement construction, are typical of engineering projects dealing with temporary works. The dewatering of excavations has the potential to be complex, with associated geotechnical risks such as flooding, watertightness, and potential partial/total collapse of retaining walls. 

Related engineering investigations, such as those to estimate flows into open excavation for choosing and sizing appropriate dewatering systems, will be demonstrated in a further example using a well-established analytical solution.

![Figure 1: Problem setting, model geometry](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/Case-study-SSS3-F1-Problem-setting-v3.png)

## Conditions used

The ground and the cut-off wall/structures as materials are assumed to be simple hydraulic head boundary conditions, with a constant infiltration rate mimicking the impact of rain or local flooding conditions.
>
> - Our example model geometry is based on the problem published in, *Soil Mechanics*, by Lambe and Whitman (1969) and attempts to assess seepage flow in the foundation of a concrete dam with a cut-off wall. 
>
> - No parametric nor sensitivity analyses were undertaken on this model.

## Assumptions

 A sand-type material is assumed, and this is reflected in the choice of its average homogeneous and isotropic hydraulic conductivity.

 ![Table 1: Material Properties](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/Case-study-SSS4-T1-Material-properties.png)

![Table 2: Boundary conditions](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/Case-study-SSS4-T2-Boundary-conditions.png)

## Comparison of results / Conclusion

### Gofer, Oasys Slope, Plaxis and SEEP/W

The model geometry consists of a basement excavation with symmetrical cut-off walls on each side. The relatively thin cut-off walls (0.5m) are modelled as a lower permeability material. The difference in hydraulic conductivity between the soil and the cut-off walls is 2 orders of magnitude.

The boundary conditions on the vertical edges represent the effective hydraulic head, i.e., 19m. The infiltration rate is included on a second stage, simulating potential flooding. The results obtained are compared with the non-infiltration rate stage counterpart.

![Figure 2: Hydraulic head calculation results for Gofer, Plaxis, SEEP/W and Slope (no infiltration)](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/Case-study-SSS4-F2-Hydraulic-Head-No-Infiltration.png)

![Figure 3: Hydraulic head calculation results for Gofer, Plaxis, SEEP/W and Slope (with infiltration)](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/Case-study-SSS4-F3-Hydraulic-Head-Infiltration.png)

![Figure 4: Porewater pressures calculation results for Gofer, Plaxis, SEEP/W and Slope (no infiltration)](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/Case-study-SSS4-F4-Porewater-Pressures-No-Infiltration.png)

![Figure 5: Porewater pressures calculation results for Gofer, Plaxis, SEEP/W and Slope (with infiltration)](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/Case-study-SSS4-F5-Porewater-Pressures-Infiltration.png)
