# powerBI-template
A Power BI template showcasing a solution-oriented approach to select building materials in early design phase.

![solution-oriented configurator PoC_overview](https://github.com/user-attachments/assets/2e981bb0-d5d2-469d-8050-022c44fd68ff)
*Figure: Overview page of the dashboard*


# 1. Why

Usually we start with a predetermined building design and material selection before calculating CO2 or costs. That can sometimes be limiting, as it reduces flexibility and may overlook more sustainable or cost-effective alternatives.

This template flips the approach: **here we begin with sustainability ambitions and an open mind, and then we explore what our options are to meet those ambitions**.

It is also about making informed decisions. We want to understand the impact of our choices on what we find important -- such as CO2 emission, cost, time -- and evaluate potential trade-offs among them to make better decisions early in the process.

*** **In short, more flexibility, better insights, better decisions.** ***

# 2. What

**A proof-of-concept dashboard in Power BI.** 

- This dashboard takes **as key indicators CO2, MPG (Milieu Prestatie Gebouwen), and material cost**.
- It uses **as input** a 3D building model, a data sheet on how much those three indicators are associated with different material choices.
- It shows **as result** an integrated graph (a parallel coordinate plot) on how four preset material combinations (or, "opties") perform on those three indicators. All preset material combinations are *modifiable*, and the new values are reflected real-time in the graph.

![solution-oriented configurator PoC_optie3](https://github.com/user-attachments/assets/e196032a-95c6-4828-8366-6ce42c722b3c)

*Figure: Page for viewing and modifying individual options*


## 2.1 Terms

**Life span [levensduur, in years]:** used in MPG and CO2 calculation. As Power BI parameters.

**BVO [gross floor area, in m2]:** used in MPG and CO2 calculation. As Power BI parameters. In future, a dummy element can be used if the area is to be read into Power BI from the model, e.g. a dummy room or floor.

**MPG:** Milieu Prestatie Gebouwen

**MKI:** Milieukostenindicator




## 2.2 Calculations

**Embedded CO2 = sum of embedded CO2 of all elements / BVO**

**MPG = sum of MKI of all elements / BVO / life span**

**Material cost = sum of cost of all elements**


## 2.3 Important assumptions

**1. Conversion of quantities for different materials**

For some building components, when its material is changed, the quantity of material changes too. For example, concrete columns have certain cross-sectional sizes and follow the grid of certain size, and such cross-sectional sizes and/or grid size would be different for steel columns.

Here it is assumed that the building model is designed with certain material assumptions, concrete columns in this example project.

The conversion in material quantity can be found in page "auxilary".

**2. Element-based calculation**

It is assumed that the value of the key indicators are proportional to volumes of building elements. Note that, unlike MPG and embedded CO2, material cost is not entirely based on the volumnes of material. You may want to customise the cost calculation rules to suit your need.


# 3. How to use the template
## 3.1 Prerequisites

To edit:

- Power BI Desktop
- Speckle 3D Viewer Visual for Power BI ([guide](https://speckle.systems/tutorials/installing-3d-viewer-visual-for-power-bi/))



# 4. Disclaimers

- The CO2, MKI and cost numbers in database file are for demonstration purpose; they should not be regarded as actual data. You may refer to other sources for actual data, e.g. [Nationale Milieudatabase](https://milieudatabase.nl/nl/).
- This is a personal project; the views and practices expressed are my own and do not necessarily reflect those of my employer.

