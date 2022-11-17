# C-phi analysis validation

## Summary

We tested Gofer’s c-phi analysis feature by modelling a cutting into multiple horizontal soil strata. This example looks at two key areas: **Factor of Safety (FoS)** and potential **failure surfaces**, to determine how our results compared with other studies.

Our example model is taken from [Chowdhury and Xu, 2005](https://www.sciencedirect.com/science/article/abs/pii/095183209400063T), which was also referecned in a joint Arup-Oasys study [(_Ground Engineering, 2014_)](https://www.researchgate.net/publication/279176042_Slope_stability_analysis_-_limit_equilibrium_or_the_finite_element_method) comparing **limit equilibrium** (LE) and **finite element** (FE) methods using Oasys Slope (LE) and Oasys Safe (FE).

The model consists of three soil layers with parameters and geometries as shown below:

_Table 1: Material parameters_

| Material      | Young's modulus (Pa)      | Poisson's ratio | Cohesion (kPa) | Friction angle $(\degree)$ | Density (kN/m<sup>3</sup>) |
| ------------- | ------------------------- | --------------- | -------------- | -------------------------- | -------------------------- |
| Soil 1 (Sand) | 1 $\times$ 10<sup>5</sup> | 0.3             | 3              | 30                         | 21                         |
| Soil 2 (Clay) | 1 $\times$ 10<sup>5</sup> | 0.3             | 22             | 11                         | 22                         |
| Soil 3 (Clay) | 1 $\times$ 10<sup>5</sup> | 0.3             | 25             | 20                         | 22                         |

## What is it?

C-phi analysis is a method commonly used in geotechnical **finite element analyses** (FEA). Soil strength is gradually reduced until failure is reached. An implied factor of safety is calculated as the inverse of the reduction ratio at failure.

The likely failure surface (or surfaces) can be visualised by inspecting soil results, aiding understanding of how the soil body might fail.

The major advantage of c-phi analysis is that it finds the failure surface(s), rather than testing predefined potential failure surfaces, as is the case with limit equilibrium.

_Geometries and fixities as modelled in Gofer_

![soil](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/soil-graph.png)

## C-phi in Gofer

You will find Gofer's c-phi analysis feature in the **Configure stages** mode, available as a calculation type within **Stage settings**.

Results are presented in the mesh and as a graph, plotting maximum displacement as strength is reduced.

_A c-phi reduction graph available in Gofer_

![c-phi-graph](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/c-phi-graph.png)

### How it compares: FoS

_Table 2: Factor of Safety, as compared across software_

| Gofer c-phi | Chowdhury and Xu | Oasys Slope | Oasys Safe |
| ----------- | ---------------- | ----------- | ---------- |
| FoS = 1.12  | FoS = 1.16       | FoS = 1.21  | FoS = 1.20 |

This table demonstrates that Gofer's derived FoS compares favourably with the other software packages referenced.

### How it compares: Slip surfaces

The slip surface results from the LE and FE methods **compared favourably**, with the LE method limited to circular slips. Only FE modelling revealed a potential second slip surface. This may have been missed when searching for the lowest FoS in Oasys Slope alone.

When using LE, the larger slip surface is immediately visible, but the second slip surface is only detected by examining other slip surfaces.
