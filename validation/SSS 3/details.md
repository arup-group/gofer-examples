# Steady state seepage part 3: Dam with cut-off wall

## Summary

We tested Gofer’s **steady state seepage (SSS)** features by modelling a homogeneous, single layer medium, with isotropic materials for both the soil and the cut-off wall.
Seepage analysis is a familiar issue for those working in dam and reservoir engineering, and this model demonstrates Gofer's performance and results.

We validated our results and compared them across **Gofer, Oasys Slope, Plaxis** and **SEEP/W**.  

## Background

Cut-off walls under a dam structure are engineering solutions required for a variety of reasons:  

> - If the dam is required to be installed/constructed over pervious geomaterials, a cut-off wall prevents excessive seepage that can undermine the structure's stability and have a detrimental impact on the downstream watercourses.
>
> -  Cut-off walls act as seepage barriers to isolate areas both upstream – by retaining water in the dam’s reservoir – and downstream, protecting the river.
> - Cut-off walls can be constructed from a variety of materials and using a range of methods: diaphragm walls, steel sheet pile, pile walls, jet grouting, masonry/concrete, deep soil mixing, etc. These provide different levels of protection. 

![Figure 1: Problem setting](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/Case-study-SSS3-F1-Problem-setting​-v3.png)

## Conditions used

We used simple hydraulic head boundary conditions for the ground and cut-off wall / structure.

The model geometry is taken from the book, *Soil Mechanics*, by Lambe and Whitman (1969) and represents steady state seepage flow in the foundation of a concrete dam with a cut-off wall. 

The model geometry does not explicitly consider the dam sitting on top of the permeable geomaterial. A relatively thin cut-off wall (1m) is modelled as a lower permeability material under the footprint of the dam. It is located under the idealised upstream edge of the dam foundation.

The boundary conditions on each side of the dam represent the effective hydraulic head, i.e. 60m upstream and 40m downstream. The difference in hydraulic conductivity between the two materials is 5 orders of magnitude.

## Assumptions

![Table 1: Material properties](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/Case-study-SSS3-T1-Material-properties.png)

![Table 2: Boundary conditions](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/Case-study-SSS3-T2-Boundary-conditions.png)

## Comparison of Results / Conclusion

### Gofer, Oasys Slope, Plaxis and SEEP/W

Gofer's analysis delivered values consistent with this mode in Oasys Slope, Plaxis and SEEP/W for both the hydraulic head and porewater pressure results/output.

As you can see in the following figures, (F2 and F3) the computed solutions in Gofer delivered results that compare favourably with the established software products in this field, Oasys Slope, Plaxis and SEEP/W.

![Figure 2: Hydraulic head calculation and results for Gofer, Plaxis, SEEP/W and Slope](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/Case-study-SSS3-F2-Comparison-Hydraulic-Head.png)

![Figure 3: Porewater pressures calculation results for Gofer, Plaxis, SEEP/W and Slope](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/Case-study-SSS3-F3-Porewater-Pressures.png)
