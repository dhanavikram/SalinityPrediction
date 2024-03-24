# Prediction of Water Salinity Levels

Salinity plays a key role in analyzing the water cycle, ocean circulation, and climate change, as it driving ocean currents and circulation patterns. Variations in salinity affect the density of seawater, which in turn influences its movement and mixing. Many marine organisms have adapted to specific salinity levels, so variations in salinity can directly impact their distribution, reproduction, and survival.

CTD stands for conductivity, temperature, and depth, and refers to a package of electronic instruments that measure oceanographic properties (i.e., the physical features of seawater such as salinity, dissolved oxygen, chlorophyll-a, nutrients, and many more). A CTD cast gives scientists a precise and comprehensive charting of the distribution and variation of water oceanographic properties that helps to understand how the oceans affect life. `CalCOFI.csv` contains a subset of data from the CalCOFI dataset that represents the longest (1949-present) and most complete (more than 50,000 sampling stations) time series of oceanographic and larval fish data captured in the world. This database contains oceanographic data measured using CTD casts from seawater samples collected at CalCOFI stations.

In this notebook, the goal is to design a machine learning model that estimates water salinity based on biochemical oceanographic measurements and measurement year. Data contains 325,281 measurements sampled between 1980-2016.

### Features

1. Salnty: Salinity (Practical Salinity Scale 1978) (outcome) 
2. Depthm: cast depth in meters
3. O2mlL: Milliliters oxygen per liter of seawater
4. STheta: Potential Density (Sigma Theta), Kg/M3
5. O2Sat: Oxygen percent saturation
6. Oxyμmol/Kg: Oxygen micromoles per kilogram seawater
7. ChlorA: Migrograms Chlorophyll-a per liter seawater, measured fluorometrically 
8. Phaeop: Micrograms Phaeopigment per liter seawater, measured fluormetrically 
9. PO4uM: Micromoles Phosphate per liter of seawater
10. SiO3uM: Micromoles Silicate per liter of seawater
11. NO2uM: Micromoles Nitrite per liter of seawater
12. NH3uM: Micromoles Ammonia per liter of seawater
13. C14As1: 14C Assimilation of Replicate 1 (milligrams carbon per cubic meter of seawater per half light day)
14. C14As2: 14C Assimilation of Replicate 2 (milligrams carbon per cubic meter of seawater per half light day)
15. DarkAs: 14C Assimilation of Dark/Control Bottle (milligrams carbon per cubic meter of seawater per half light day)
16. LightP : Light intensities of the incubation tubes in the primary productivity experiment, expressed as percentages
17. Year: The year the sample was collected

### Train/Val/Test Split

The training data will include samples collected between 1980 to 2010. The development data will include samples collected between 2011 to 2013. Finally, the testing data will include samples collected between 2014 to 2016.
