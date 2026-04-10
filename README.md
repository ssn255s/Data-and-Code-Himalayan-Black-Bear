# Data-and-Code-Himalayan-Black-Bear
Data and Code Description for "Are Anthropogenic Factors Altering Distribution of Himalayan Black Bears in Nepal?"
Project Overview

This repository contains all data and scripts used to develop models for Ursus thibetanus in Nepal. Two modeling frameworks were implemented to evaluate the influence of environmental and anthropogenic factors on species distribution:

Natural Environment Model (NEM) – based solely on environmental (bioclimatic and habitat) variables
Anthropogenic Environment Model (AEM) – incorporates both environmental and anthropogenic predictors

The comparison of these models allows assessment of how human activities influence habitat suitability.

Repository Structure and File Description

📂 Data Files
Ursus_thibetanus_user.csv
Contains occurrence records used for model calibration.
Includes geographic coordinates (latitude and longitude) for presence locations of Ursus thibetanus.

Variables/ (Folder)
Contains all predictor variables initially considered for model development, including:

Bioclimatic variables (e.g., temperature and precipitation metrics)
Topographic variables (e.g., elevation, slope)
Anthropogenic variables (e.g., distance to roads, settlements, human population, livestock, water sources)

Note: These variables were processed and screened prior to final model selection (e.g., collinearity filtering).

Model Development
Maxent_model.R
R script used to construct species distribution models using the MaxEnt algorithm.
This script includes:
Data preparation
Variable selection
Model tuning and evaluation
Generation of habitat suitability predictions

Model Outputs
BioClimModel
Output representing the Natural Environment Model (NEM).
This model includes only environmental predictors and represents baseline ecological suitability.
FullModel
Output representing the Anthropogenic Environment Model (AEM).
This model includes both environmental and anthropogenic predictors and reflects realized suitability under human influence.

📂 Visualization and Analysis
Result Visualization.Rmd
R Markdown file containing all code used to generate figures and results presented in the manuscript, including:
Model performance metrics
Suitability maps
Comparative analyses between models
LULC_Plot.R
Script used to generate land-use/land-cover (LULC) based habitat suitability plots used in the manuscript.

Modeling Approach
Species distribution models were developed using presence-only occurrence data and environmental predictors.
Two model configurations were used:
Natural Environment Model (NEM) – environmental variables only
Anthropogenic Environment Model (AEM) – environmental + anthropogenic variables
Models were evaluated using standard metrics (e.g., AUC and other relevant statistics).
