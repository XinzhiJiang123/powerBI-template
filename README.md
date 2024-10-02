# powerBI-template
Power BI templates for AEC use

# Why


# What

An dashboard showing estimated CO2, MPG (MilieuPrestatie Gebouwen), and cost of preset material combinations

## Important assumptions

- The CO2, MKI (Milieukostenindicator) and cost numbers in database file are for illustration purpose; they should not be regarded as real data.

- Different quantities for different materials:
- 
For some building components, when its material is changed, the quantity of material changes too. For example, concrete columns have certain cross-sectional sizes and follow the grid of certain size, and such cross-sectional sizes and/or grid size would be different for steel columns.

Here it is assumed that the building model is designed with certain material assumptions: concrete columns in this example project.

The conversion in material quantity can be found in **parameters.


## Calculation

**Life span [levensduur, in years]:** used in MPG and CO2 calculation. As Power BI parameters.

**BVO [gross floor area, in m2]:** used in MPG and CO2 calculation. As Power BI parameters. In future, a dummy element can be used if the area is to be read into Power BI from the model, e.g. a dummy room or floor.


**CO2** = sum of CO2 of all elements / BVO

**MPG** = sum of MKI of all elements / BVO / life span

**Cost** = sum of cost of all elements

