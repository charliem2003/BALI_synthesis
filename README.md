# BALI_synthesis

Data analysis scripts for the manuscript 'Marsh *et al.* **High level ecosystem functions more resilient to tropical forest degradation and deforestation'** *in prep*

In the zip file ['BALI_synthesis_analysis.zip'](https://github.com/charliem2003/BALI_synthesis/blob/main/BALI_synthesis_analyses.zip) there are outputs from RMarkdown scripts that include all steps of the analysis for each dataset, including R code, incorporating data visualisation, exploration and standardisation, model building and evaluation, and visualisation of results.

Each dataset presented in the manuscript has an html file within the folder 'Analyses'. For datasets involving bat, bird, dung beetle and tree traits additional markdown documents are available for steps take during data preparation in the folder 'Data preparation'.

In the zip file ['BALI_synthesis_data.zip'](https://github.com/charliem2003/BALI_synthesis/blob/main/BALI_synthesis_data.zip) are .rds data files that have been cleaned, prepared and z-score standardised following the procedures outlined in the respective markdown files.

To repeat any given analysis, follow the respective rmarkdown document, excluding the data manipulation steps:

1. Read in the data file as described above:
	dd <- readRDS(paste0("path/to/rds/file/", "name_of_file.rds")) 
2. Run the code at the top of the markdown workflow (sections "Data information" and "Load in necessary libraries")
3. Do not run the sections "Read in data" through to "Visual inspection of the data"
4. Continue the analysis from the 'Modelling' section

### Level 1 - Structure & Environment
| Dataset                              | Label                        | Filename                   | Collector        |
| ---                                  | ---                          | ---                        | ---              |
| Above-ground carbon                  | Above ground carbon          | Above_ground_carbon        | Terhi Riutta     |
| Leaf-area index                      | Leaf-area index              | Leaf_area_index            | Terhi Riutta     |
| Soil temperature                     | Soil temp.                   | Soil_temperature           | Terhi Riutta     |
| Soil moisture                        | Soil moisture                | Soil_moisture              | Dafydd Elias     |
| Air temperature: Minimum             | Air temp.: Min.              | Air_temperature_minimum    | Benjamin Blonder |
| Air temperature: Mean                | Air temp.: Mean              | Air_temperature_mean       | Benjamin Blonder |
| Air temperature: Maximum             | Air temp.: Max.              | Air_temperature_maximum    | Benjamin Blonder |
| Soil bulk density                    | Soil bulk density            | Soil_bulk_density          | Dafydd Elias     |
| Soil horizon depth                   | Soil horizon depth           | Soil_horizon_depth         | Dafydd Elias     |
| Soil pH                              | Soil pH                      | Soil_pH                    | Dafydd Elias     |
| Soil nutrients: Carbon               | Soil nutrients (C)           | Soil_nutrients_C           | Dafydd Elias     |
| Soil nutrients: Nitrogen             | Soil nutrients (N)           | Soil_nutrients_N           | Dafydd Elias     |
| Soil nutrients: Inorganic Phosporous | Soil nutrients (Inorganic P) | Soil_nutrients_Inorganic_P | Dafydd Elias     |
| Soil nutrients: Carbon:Phosphorous   | Soil nutrients (C:P)         | Soil_nutrients_C_P         | Dafydd Elias     |
| Soil nutrients: Carbon:Nitrogen      | Soil nutrients (C:N)         | Soil_nutrients_C_N         | Dafydd Elias     |

### Level 2 -  Tree traits

All tree traits were collected as part of the following study (details in this table have been extracted from table S1 of that publication): S. Both, T. Riutta, C.E.T. Paine, D.M.O. Elias, R.S. Cruz, A. Jain, D. Johnson, U.H. Kritzler, M. Kuntz, N. Majalap-Lee, N. Mielke, M.X. Montoya Pillco, N.J. Ostle, Y. Arn Teh, Y. Malhi, D.F.R.P. Burslem (2019) Logging and soil nutrients independently explain plant trait expression in tropical forests. New Phytologist. 221:4, 1853–1865.

***Photosynthesis Traits***

| Dataset                                              | Label                           | Filename              |
| ---                                                  | ---                             | ---                   |
| Aggregated photosynthesis traits                     | Photosyn. traits                | Photosynthesis traits |
| δ<sup>13</sup>C                                      | δ<sup>13</sup>C                 | Traits_13C            |
| Light-saturated photosynthetic rate                  | Photosyn. rate: A<sub>sat</sub> | Traits_Asat           |
| Maximum photosynthetic rate                          | Photosyn. rate: A<sub>max</sub> | Traits_Amax           |
| Maximum photosynthetic rate: Nitrogen concentration  | Max. photosyn. rate: N(%)       | Traits_N_conc         |
| Maximum photosynthetic rate: Phosphorous mass (area) | Max. photosyn. rate: P(mass)    | Traits_Phos_area      |
| Dark respiration (Rd)                                | Dark respiration                | Traits_Dark_resp      |
| Specific leaf area (SLA)                             | Specific leaf area              | Traits_SLA            |
| Carotenoids (area)                                   | Carotenoids: Area               | Traits_Carot_area     |
| Carotenoids (mass)                                   | Carotenoids: Mass               | Traits_Carot_mass     |
| Chlorophyll a (area)                                 | Chlorophyll a: Area             | Traits_Chl_a_area     |
| Chlorophyll a (mass)                                 | Chlorophyll a: Mass             | Traits_Chl_a_mass     |
| Chlorophyll b (area)                                 | Chlorophyll b: Area             | Traits_Chl_b_area     |
| Chlorophyll b (mass)                                 | Chlorophyll b: Mass             | Traits_Chl_b_mass     |

***Nutrient Traits***

| Dataset                                              | Label                           | Filename           |
| ---                                                  | ---                             | ---                |
| Aggregated nutrient traits                           | Nutrient traits                 | Nutrient_traits    |
| δ<sup>15</sup>N                                      | δ<sup>15</sup>N                 | Traits_15N         |
| Carbon concentration                                 | Carbon conc.                    | Traits_Carbon_conc |
| Nitrogen concentration                               | Max. photosyn. rate: N(%)       | Traits_N_perc      |
| Phosphorous concentration                            | Max. photosyn. rate: P(mass)    | Traits_Phos_mass   |
| Magnesium concentration                              |  Regulat. nutrients: Total Mg   | Traits_Total_Mg    |
| Potassium concentration                              |  Regulat. nutrients: Total K    | Traits_Total_K     |
| Calcium concentration                                |  Regulat. nutrients: Total Ca   | Traits_Total_Ca    |

***Structural Traits***

| Dataset                                              | Label                           | Filename              |
| ---                                                  | ---                             | ---                   |
| Aggregated structural traits                         | Structural traits               | Structural_traits     |
| Branch specific density                              | Branch wood density             | Traits_Branch_WD      |
| Leaf cellulose concentration                         | Leaf fibre conc.: Cellul.       | Traits_Cellulose      |
| Leaf lignin concentration                            | Leaf fibre conc.: Lignin        | Traits_Lignin         |
| Leaf hemicellulose concentration                     | Leaf fibre conc.: Hemicel.      | Traits_Hemicellulose  |
| Leaf area                                            | Leaf size: Area                 | Traits_Leaf_area      |
| Leaf dry weight                                      | Leaf size: Dry wgt              | Traits_Dry_weight     |
| Leaf force to punch                                  | Leaf strength: Tough.           | Traits_Leaf_toughness |
| Leaf thickness                                       | Leaf strength: Thick.           | Traits_Leaf_thickness |
| Leaf dry matter content                              | Leaf strength: Dry mat.         | Traits_LDMC           |
| Total phenol concentration                           | Leaf defence: Phenol            | Traits_Phenol         |
| Total tannin concentration                           | Leaf defenct: Tannin            | Traits_Tannin         |

### Level 3 -  Biodiversity

| Dataset                                          | Label                         | Filename                      | Collector             |
| ---                                              | ---                           | ---                           | ---                   |
| Soil ectomycorrhizal richness                    | Soil richness: Ectomycorrhiza | Soil_richness_Ectomycorrhiza  | Dafydd Elias          |
| Soil bacterial richness                          | Soil richness: Bacteria       | Soil_richness_Bacteria        | Dafydd Elias          |
| Soil protist richness                            | Soil richness: Protists       | Soil_richness_Protist         | Dafydd Elias          |
| Soil fungal richness                             | Soil richness: Fungi          | Soil_richness_Fungi           | Dafydd Elias          |
| Leaf spectral diversity                          | Spectral diversity            | Spectral_diversity            | Matheus Nunes         |
| Liana abundance                                  | Liana abundance               | Liana_abundance               | Boris Bongalov        |
| Dung beetle abundance                            | Dung beetle abund.            | Dung_beetle_abundance         | Eleanor Slade         |
| Dung beetle diversity: richness                  | Dung beetle diversity: q=0    | Dung_beetle_diversity_q=0     | Eleanor Slade         |
| Dung beetle diversity: Shannon diversity         | Dung beetle diversity: q=1    | Dung_beetle_diversity_q=1     | Eleanor Slade         |
| Dung beetle diversity: Simpsons diversity        | Dung beetle diversity: q=2    | Dung_beetle_diversity_q=2     | Eleanor Slade         |
| Bird abundance                                   | Bird abund.                   | Bird_abundance                | Simon Mitchell        |
| Bird diversity: richness                         | Bird diversity: q=0           | Bird_diversity_q=0            | Simon Mitchell        |
| Bird diversity: Shannon diversity                | Bird diversity: q=1           | Bird_diversity_q=1            | Simon Mitchell        |
| Bird diversity: Simpsons diversity               | Bird diversity: q=2           | Bird_diversity_q=2            | Simon Mitchell        |
| Bat abundance                                    | Bat abund.                    | Bat_abundance                 | Dave Hemprich-Bennett |
| Bat diversity (small scale)                      | Bat diversity (sm scale)      | Bat_diversity_small_scale     | Dave Hemprich-Bennett |
| Bat diversity (large scale): richness            | Bat diversity (lg scale): q=0 | Bat_diversity_large_scale_q=0 | Dave Hemprich-Bennett |
| Bat diversity (large scale): Shannon diversity   | Bat diversity (lg scale): q=1 | Bat_diversity_large_scale_q=1 | Dave Hemprich-Bennett |
| Bat diversity (large scale): Simpsons diversity  | Bat diversity (lg scale): q=2 | Bat_diversity_large_scale_q=2 | Dave Hemprich-Bennett |
| Bat β-diversity: Nestedness                      | Bat β-diversity: Nested.      | Bat_beta_diversity_Nestedness | Dave Hemprich-Bennett |
| Bat β-diversity: Turnover                        | Bat β-diversity: Turn.        | Bat_beta_diversity_Turnover   | Dave Hemprich-Bennett |
| Bat β-diversity: Total                           | Bat β-diversity: Total        | Bat_beta_diversity_Total      | Dave Hemprich-Bennett |

### Level 4 -  Functioning

| Dataset                   | Label                | Filename             | Collector     |
| ---                       | ---                  | ---                  | ---           |
| Soil respiration          | Respiration: Soil    | Soil_respiration     | Terhi Riutta  |
| Stem respiration          | Respiration: Stem    | Stem_respiration     | Terhi Riutta  |
| Net primary productivity  | NPP                  | NPP                  | Terhi Riutta  |
| Litterfall                | Litterfall           | Litterfall           | Terhi Riutta  |
| Leaf litter decomposition | Litter decomposition | Litter_decomposition | Sabine Both   |
| Dung removal              | Dung removal         | Dung_removal         | Eleanor Slade |
