# Models in DIGITbrain

## Introduction

A Db Model is a description of a given behaviour of an Industrial Product (IP) according to its characteristics and operation conditions. The creation of a model could be either manual (file editing) or automatic (obtained from processing / analysing data / simulation results describing the behaviour of a system). A Model instance describes the specific behaviour of one particular IP Instance, by leveraging actual Data and available compatible Algorithm(s). By executing the Algorithm with the actual Data, the Model instance is evaluated by the corresponding Algorithm’s Microservice and generates insights on the IP behaviour.

## Pre-requisites

Models must be accessible from Algorithms for evaluation, thus they must be located in the specific DIGITbrain Model repository.

## Metadata describing Models

For a closer look at this metadata, use the following resources:

- [Attribute Listing](attributes/model.md) for an itemised listing of fields
- [Metadata Table](tables/model.md) for a table-formatted overview

## Further reading...

This section takes an in-depth look at some of the **Parameters** fields required to describe this asset:

`In-slots` and `Outputs`

These fields have the same structure, detailed below. They include, as an array of objects, all inputs and parameters (_In-slots_) or _Outputs_ to be defined for the Model to be evaluated, such as:

* `Key` This field is of the type of group.key, e.g., type.name of each variable
* `Name` This is a human-readable name of the variable
* `Dimensions` This field describes the number of dimensions of the variable to treat it as a scalar, a vector field, etc.
* `Is-continuous` This field describes whether the variable is continuous or discrete
* `Units` This field contains several subkeys, as it follows
  * `Unit` This field indicates the unit of measurement of the variable (e.g., s, Pa, m/s, etc.)
  * `Exponents` This field contains an array of numbers defining exponents for the 7 base SI units, i.e., Length - meter (m), Time - second (s), Amount of substance - mole (mole), Electric current - ampere (A), Temperature - Kelvin (K), Luminous intensity - candela (cd), Mass - kilogram (kg). For example the derived 
 For example _N_ would be represented by the array {1, -2, 0, 0, 0, 0, 1}
  * `Offset` This field contains the offset scale, if needed (e.g., K to ºC conversion)
  * `Scale` This field describes the order of magnitude of the measurement unit scale, e.g., 10^-3 for values expressed mm         
* `Default-value` This field contains the default value for variable
* `Ranges` This field is an array containing both max and min values of the variable

    === "In-slots"
    
      ``` yaml
      Key:
      Name:
      Dimensions:
      Is-continuous:
      Units:
        Unit:
        Exponents:
        Offset:
        Scale:
      Default-value:
      Ranges:
      ```
    
    === "Outputs"
    
      ``` yaml
      Key:
      Name:
      Dimensions:
      Is-continuous:
      Units:
        Unit:
        Exponents:
        Offset:
        Scale:
      Default-value:
      Ranges:
      ```
    
`CosimSolverInfo`

:   **Optional:** This object is made up of several fields that are optional and only needed in case of co-simulation `Type` (**Description** field) only. The additional fields needed in co-simulation are:
* `Dependant FMUs` Contains a field with an array of URI for dependant FMU localisation
* `OS Requirements` Contains a set of fields defining OS requirements for co-simulation
* `Hardware Requirements` Contains a set of fields defining Hardware requirements for co-simulation

    === "Dependant FMUs"
    
      ``` yaml
      Dependencies:
      ```
    
    === "OS Requirements"
    
      ``` yaml
      Key:
      osArch:
      osType: 
      osDistribution:
      ```
      
    === "Hardware Requirements"
    
      ``` yaml
      recommendedNumberOfGPUCores:
      minimumNumberOfGPUCores:
      recommendedGPURAM:
      minimumGPURAM:
      recommendedRAM:
      minimumRAM:
      recommendedCPUs:
      minimumCPUs:
      requiredDiskSpace:
      ```
