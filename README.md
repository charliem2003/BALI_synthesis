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
| Dataset                              | Label                        | Collector        |
| ---                                  | ---                          | ---              |
| Above-ground carbon                  | Above ground carbon          | Terhi Riutta     |
| Leaf-area index                      | Leaf-area index              | Terhi Riutta     |
| Soil temperature                     | Soil temp.                   | Terhi Riutta     |
| Soil moisture                        | Soil moisture                | Dafydd Elias     |
| Air temperature: Minimum             | Air temp.: Min.              | Benjamin Blonder |
| Air temperature: Mean                | Air temp.: Mean              | Benjamin Blonder |
| Air temperature: Maximum             | Air temp.: Max.              | Benjamin Blonder |
| Soil bulk density                    | Soil bulk density            | Dafydd Elias     |
| Soil horizon depth                   | Soil horizon depth           | Dafydd Elias     |
| Soil pH                              | Soil pH                      | Dafydd Elias     |
| Soil nutrients: Carbon               | Soil nutrients (C)           | Dafydd Elias     |
| Soil nutrients: Nitrogen             | Soil nutrients (N)           | Dafydd Elias     |
| Soil nutrients: Inorganic Phosporous | Soil nutrients (Inorganic P) | Dafydd Elias     |
| Soil nutrients: Carbon:Phosphorous   | Soil nutrients (C:P)         | Dafydd Elias     |
| Soil nutrients: Carbon:Nitrogen      | Soil nutrients (C:N)         | Dafydd Elias     |

### Level 2 -  Tree traits

All tree traits were collected as part of the following study (details in this table have been extracted from table S1 of that publication): S. Both, T. Riutta, C.E.T. Paine, D.M.O. Elias, R.S. Cruz, A. Jain, D. Johnson, U.H. Kritzler, M. Kuntz, N. Majalap-Lee, N. Mielke, M.X. Montoya Pillco, N.J. Ostle, Y. Arn Teh, Y. Malhi, D.F.R.P. Burslem (2019) Logging and soil nutrients independently explain plant trait expression in tropical forests. New Phytologist. 221:4, 1853–1865.

***Photosynthesis Traits***

| Dataset                                              | Label                           |
| ---                                                  | ---                             |
| Aggregated photosynthesis traits                     | Photosyn. traits                |
| δ<sup>13</sup>C                                      | δ<sup>13</sup>C                 |
| Light-saturated photosynthetic rate                  | Photosyn. rate: A<sub>sat</sub> |
| Maximum photosynthetic rate                          | Photosyn. rate: A<sub>max</sub> |
| Maximum photosynthetic rate: Nitrogen concentration  | Max. photosyn. rate: N(%)       |
| Maximum photosynthetic rate: Phosphorous mass (area) | Max. photosyn. rate: P(mass)    |
| Dark respiration (Rd)                                | Dark respiration                |
| Specific leaf area (SLA)                             | Specific leaf area              |
| Carotenoids (area)                                   | Carotenoids: Area               |
| Carotenoids (mass)                                   | Carotenoids: Mass               |
| Chlorophyll a (area)                                 | Chlorophyll a: Area             |
| Chlorophyll a (mass)                                 | Chlorophyll a: Mass             |
| Chlorophyll b (area)                                 | Chlorophyll b: Area             |
| Chlorophyll b (mass)                                 | Chlorophyll b: Mass             |

***Nutrient Traits***

| Dataset                                              | Label                           |
| ---                                                  | ---                             |
| Aggregated nutrient traits                           | Nutrient traits                 |
| δ<sup>15</sup>N                                      | δ<sup>15</sup>N                 |
| Carbon concentration                                 | Carbon conc.                    |
| Nitrogen concentration                               | Max. photosyn. rate: N(%)       |
| Phosphorous concentration                            | Max. photosyn. rate: P(mass)    |
| Magnesium concentration                              |  Regulat. nutrients: Total Mg   |
| Potassium concentration                              |  Regulat. nutrients: Total K    |
| Calcium concentration                                |  Regulat. nutrients: Total Ca   |

***Structural Traits***

| Dataset                                              | Label                           |
| ---                                                  | ---                             |
| Aggregated structural traits                         | Structural traits               |
| Branch specific density                              | Branch wood density             |
| Leaf cellulose concentration                         | Leaf fibre conc.: Cellul.       |
| Leaf lignin concentration                            | Leaf fibre conc.: Lignin        |
| Leaf hemicellulose concentration                     | Leaf fibre conc.: Hemicel.      |
| Leaf area                                            | Leaf size: Area                 |
| Leaf dry weight                                      | Leaf size: Dry wgt              |
| Leaf force to punch                                  | Leaf strength: Tough.           |
| Leaf thickness                                       | Leaf strength: Thick.           |
| Leaf dry matter content                              | Leaf strength: Dry mat.         |
| Total phenol concentration                           | Leaf defence: Phenol            |
| Total tannin concentration                           | Leaf defenct: Tannin            |

### Level 3 -  Biodiversity

| Dataset                                          | Label                         | Collector             |
| ---                                              | ---                           | ---                   |
| Soil ectomycorrhizal richness                    | Soil richness: Ectomycorrhiza | Dafydd Elias          |
| Soil bacterial richness                          | Soil richness: Bacteria       | Dafydd Elias          |
| Soil protist richness                            | Soil richness: Protists       | Dafydd Elias          |
| Soil fungal richness                             | Soil richness: Fungi          | Dafydd Elias          |
| Leaf spectral diversity                          | Spectral diversity            | Matheus Nunes         |
| Liana abundance                                  | Liana abundance               | Boris Bongalov        |
| Dung beetle abundance                            | Dung beetle abund.            | Eleanor Slade         |
| Dung beetle diversity: richness                  | Dung beetle diversity: q=0    | Eleanor Slade         |
| Dung beetle diversity: Shannon diversity         | Dung beetle diversity: q=1    | Eleanor Slade         |
| Dung beetle diversity: Simpsons diversity        | Dung beetle diversity: q=2    | Eleanor Slade         |
| Bird abundance                                   | Bird abund.                   | Simon Mitchell        |
| Bird diversity: richness                         | Bird diversity: q=0           | Simon Mitchell        |
| Bird diversity: Shannon diversity                | Bird diversity: q=1           | Simon Mitchell        |
| Bird diversity: Simpsons diversity               | Bird diversity: q=2           | Simon Mitchell        |
| Bat abundance                                    | Bat abund.                    | Dave Hemprich-Bennett |
| Bat diversity (small scale)                      | Bat diversity (sm scale)      | Dave Hemprich-Bennett |
| Bat diversity (large scale): richness            | Bat diversity (lg scale): q=0 | Dave Hemprich-Bennett |
| Bat diversity (large scale): Shannon diversity   | Bat diversity (lg scale): q=1 | Dave Hemprich-Bennett |
| Bat diversity (large scale): Simpsons diversity  | Bat diversity (lg scale): q=2 | Dave Hemprich-Bennett |
| Bat β-diversity: Nestedness                      | Bat β-diversity: Nested.      | Dave Hemprich-Bennett |
| Bat β-diversity: Turnover                        | Bat β-diversity: Turn.        | Dave Hemprich-Bennett |
| Bat β-diversity: Total                           | Bat β-diversity: Total        | Dave Hemprich-Bennett |


### Level 4 -  Functioning

| Dataset                   | Label                | Collector     |
| ---                       | ---                  | ---           |
| Soil respiration          | Respiration: Soil    | Terhi Riutta  |
| Stem respiration          | Respiration: Stem    | Terhi Riutta  |
| Net primary productivity  | NPP                  | Terhi Riutta  |
| Litterfall                | Litterfall           | Terhi Riutta  |
| Leaf litter decomposition | Litter decomposition | Sabine Both   |
| Dung removal              | Dung removal         | Eleanor Slade |
