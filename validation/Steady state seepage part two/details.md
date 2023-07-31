## Steady state seepage example model: Part 2

### Summary

This example model continues the validation study we began in **Steady state seepage validation: Part 1**.

In Part 1, we tested Gofer’s **steady state seepage** features by modelling a heterogeneous earth dam, with isotropic materials, placed on top of an assumed horizontal impervious layer.

In this example, the dam flanks of our structure are made of silty _sand_ while the core is assumed to be a less permeable material, such as _clay_. The geometry, boundary conditions and the drain at the downstream toe are all identical to the model presented in Part 1.

This example is used to make a comparison of results from **Gofer, Oasys Slope, Plaxis** and **SEEP/W**.

### Source material and background

Our example model geometry is taken from _Groundwater and Seepage_, Milton E. Harr (1962; rev. 1990, section 8.6).

Harr presents the case of an earth dam, with no low permeability core. The dam is composed of a single material with isotropic hydraulic conductivity, on top of an impervious base. A toe filter is installed at the downstream side.

The revised model used here introduces a _low permeability core_. Harr's analytical solution is no longer applicable because the model geometry and parameters have changed.

The introduction of an isotropic low hydraulic conductivity material at the dam core is common practice by dam engineers who frequently face this problem.

### Parameters

We conducted a sensitivity analysis under different scenarios, analysing the behaviour of the groundwater pressures within the dam body. The assumed changes in hydraulic conductivity, **K**, at the dam core are presented in the following summary of geometry and key parameters.

_Table 1: Material types and associated permeabilities_

![table](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/Table-ss-part2v2.png)

![cross-section](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/Slide-1-original-sss-validation-model.png)

_Graph showing dam cross-section and toe drain/filter_

### How it compares: Oasys Slope, Plaxis and SEEP/W

The computed analytical solution for this comparison study is a match with Gofer, Oasys Slope, Plaxis and SEEP/W for most scenarios.

In cases where the dam core material is 5x and 10x lower, the different implementation of the Finite Element solver solutions may account for some slight discrepancies. These discrepancies will be more obvious for larger ratios of Kflanks / Kcore.

### Results

The porewater pressure results obtained from Oasys Slope, Plaxis and SEEP/W are also a like-for-like match with Gofer for the scenarios with no core and 2x hydraulic conductivity at the dam core.

The figures shown below include the computed solutions in Gofer, Oasys Slope, Plaxis and SEEP/W for all scenarios.

![no-core](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/f2-nocore-gfr-plx-seep-slope2.png)
_Analysis results: No core_

![2-core](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/f3-2xcore-gfr-plx-seep-slope.png)
_Analysis results: 2x K core reduction_

![5-core](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/f4-5xcore-gfr-plx-seep-slope.png)
_Analysis results: 5x K core reduction_

![10-core](https://b2c-templates-arup.s3-eu-west-1.amazonaws.com/gofer/validationImages/f5-10xcore-gfr-plx-seep-slope.png)
_Analysis results: 10x K core reduction_
