# Evaluating Normality of Rodent Hindfoot Length

**Author:** Nathalie Garcia  
**Last updated:** 05 August 2024
You may view the fully rendered report here:
https://rpubs.com/Nathalie-Gar/1314114

## Overview

This project investigates whether the hindfoot length of rodents, stratified by sex and species, follows a normal distribution. Data come from the long-term “Portal Project” desert ecosystem study and are accessed via the `ratdat` R package

## Data Source

- **Portal Project dataset** (40 years of monthly rodent trapping in Portal, Arizona)  
- Measurements include species, sex, and hindfoot length  
- Accessible in R through:
  ```r
  install.packages("ratdat")
  library(ratdat)
  data("complete", package = "ratdat")



