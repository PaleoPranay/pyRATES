# pyRATES Workshop: Python and R Analysis of Time SerieS
#### Date: 03 - 06 June 2024
---------------------------------------------
#### This repository has been created to reproduce a study
---------------------------------------------
 **Title of the study:** Five million years of Antarctic Circumpolar Current strength variability

**Authors:** Frank Lamy, Gisela Winckler, Helge W. Arz, Jesse R. Farmer, Julia Gottschalk, Lester Lembke-Jene, Jennifer L. Middleton, Michèlle van der Does, Ralf Tiedemann, Carlos Alvarez Zarikian, Chandranath Basak, Anieke Brombacher, Levin Dumm, Oliver M. Esper, Lisa C. Herbert, Shinya Iwasaki, Gaston Kreps, Vera J. Lawson, Li Lo, Elisa Malinverno, Alfredo Martinez-Garcia, Elisabeth Michel, Simone Moretti, Christopher M. Moy, Ana Christina Ravelo, Christina R. Riesselman, Mariem Saavedra-Pellitero, Henrik Sadatzki, Inah Seo, Raj K. Singh, Rebecca A. Smith, Alexandre L. Souza, Joseph S. Stoner, Maria Toyos, Igor M. Venancio P. de Oliveira, Sui Wan, Shuzhuang Wu & Xiangyu Zhao 

**Link to the paper:** [https://doi.org/10.1038/s41586-024-07143-3](https://doi.org/10.1038/s41586-024-07143-3)

**Link to the original dataset:** [https://doi.org/10.1594/PANGAEA.965443](https://doi.org/10.1594/PANGAEA.965443)

------------------------------------------------
**Objectives:** To reproduce the following figure.

<div align="center">
  <img src="https://media.springernature.com/full/springer-static/esm/art%3A10.1038%2Fs41586-024-07143-3/MediaObjects/41586_2024_7143_Fig14_ESM.jpg?as=webp" alt="Extended Data Fig. 9: Long-term ACC changes on approximately 400-kyr timescales.">
</div>


[Link to the figure](https://media.springernature.com/full/springer-static/esm/art%3A10.1038%2Fs41586-024-07143-3/MediaObjects/41586_2024_7143_Fig14_ESM.jpg?as=webp)

------------

### **Proposed workflow:**
| Steps | Explanation | Available links |
|-------| ------------| ----------|
| **1. Gather Data** | Loading all the given datasets as pyleo series | [Dataset](https://doi.org/10.1594/PANGAEA.965443)|
| **2. Data Processing**| Process data for any missing values, interpolation to deal with unevenly spaced data etc. | [Data cleaning steps](https://pyleoclim-util.readthedocs.io/en/latest/core/api.html#pyleoclim.core.series.Series.clean) |
| **3. Spectral Analysis** | Perform spectral analysis on loaded series using pyleoclim package. | [Pyleoclim](https://pyleoclim-util.readthedocs.io/en/latest/)|
| **4. Filtering Timeseries**| Filter the timeseries for 413kyr periodicity.| [Filtering using pyleoclim](http://linked.earth/PyleoTutorials/notebooks/L1_filtering_and_detrending.html) |
| **5. Stackplot**| Create a stackplot combining all the timeseries to generate the final figure. | Function: [stackplot()](https://pyleoclim-util.readthedocs.io/en/v0.7.4/utils/plotting/stackplot.html) |







