# powerBI-template
A Power BI template showcasing a solution-oriented approach to select building materials in early design phase.

# Why

Usually we start with a predetermined building design and material selection before calculating CO2 or costs. That can sometimes be limiting, as it reduces flexibility and may overlook more sustainable or cost-effective alternatives.

This template flips the approach: here we begin with sustainability ambitions and an open mind, and then we explore what our options are to meet those ambitions.

It is also about making informed decisions. We want to understand the impact of our choices on what we find important -- such as CO2 emission, cost, time -- and evaluate potential trade-offs among them to make better decisions early in the process.

# What

A proof-of-concept dashboard in Power BI. 

- This dashboard takes CO2, MPG (Milieu Prestatie Gebouwen), and material cost as the key indicators.
- It uses as input a 3D building model, a data sheet on how much those three indicators are associated with different material choices.
- It shows as result an integrated graph on how four preset material combinations (or, "opties") perform on those three indicators. All preset material combinations are modifiable, and the new key indicator values are reflected real-time in the graph.


**"Overview" page:** shows a 3D visualisation of the imported building model, project information, and a parallel coordinate plot with embedded CO2, 
The key factors:
An dashboard showing estimated CO2, MPG (MilieuPrestatie Gebouwen), and cost of preset material combinations.



# How to use

## Prerequisit

To edit:

- Power BI Desktop
- Speckle connector for Power BI
- 

## Terminology and calculation

### Terms

**Life span [levensduur, in years]:** used in MPG and CO2 calculation. As Power BI parameters.

**BVO [gross floor area, in m2]:** used in MPG and CO2 calculation. As Power BI parameters. In future, a dummy element can be used if the area is to be read into Power BI from the model, e.g. a dummy room or floor.

### Calculation
**Embedded CO2 = sum of embedded CO2 of all elements / BVO**

**MPG = sum of MKI of all elements / BVO / life span**

**Cost = sum of cost of all elements**

Note that, unlike MPG and embedded CO2, material cost is not entirely based on the volumnes of material. You may want to customise the cost calculation rules to suit your need.

- Different quantities for different materials:
- 
For some building components, when its material is changed, the quantity of material changes too. For example, concrete columns have certain cross-sectional sizes and follow the grid of certain size, and such cross-sectional sizes and/or grid size would be different for steel columns.

Here it is assumed that the building model is designed with certain material assumptions: concrete columns in this example project.

The conversion in material quantity can be found in **parameters.

## Important assumptions

- The CO2, MKI (Milieukostenindicator) and cost numbers in database file are for illustration purpose; they should not be regarded as real data.

