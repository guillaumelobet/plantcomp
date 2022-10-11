# FSPM workshop

In this workshop, we will learn how to use basic functions of a functional-structural plant model. For the strucural part (creation of the architecture), we will use the model CPlantBox. We will then use the model MARSHAL to simulate water flow in the structure. 

## CPlantBox plant model

CPlantBox is a model used to simulated the growth and development of complex plant. Here we will use it to simulate a root system architecture. The source code of the model can be found here https://github.com/Plant-Root-Soil-Interactions-Modelling/CPlantBox

### Shiny App

For a first try, we will use a user-friendly web interface to get to know the different parameters of the model.

ShinyApp : https://plantmodelling.shinyapps.io/shinyRootBox/

### Python interface

To go further, we have developped a Python interface to interact with our C++ model

Colab : https://colab.research.google.com/github/water-fluxes/day-3-plant-scale-cplantbox/blob/main/1_cplantbox.ipynb

To make a full plant, change 

    # Create instance describing a root system
    rs = pb.RootSystem()
    path = "../../../modelparameter/rootsystem/"
    name = "Zea_mays_1_Leitner_2010"

by

    # Open plant and root parameter from a file
    rs = pb.Plant()
    path = "../../../modelparameter/plant/"
    name = "Triticum_aestivum_adapted_2021"

## MARSHAL hydraulic model

MARSHAL takes to output of CPlantBox (the root architecture file) top compute the water flow in the system and compute macro properties

## Play with the model and the parameters

For a first try, we will use a user-friendly web interface to get to know the different parameters of the model.

ShinyApp : [https://plantmodelling.shinyapps.io/shinyRootBox/](https://plantmodelling.shinyapps.io/marshal/)

## R interface

MARSHAL is developped in R and can directly be used in any R compliant interface. Example in this binder : 

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/water-fluxes/day-3-plant-scale-marshal/HEAD)


