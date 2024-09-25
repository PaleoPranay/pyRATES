# pyRATES Workshop: Python and R Analysis of Time SerieS
#### Date: 03 - 06 June 2024
---------------------------------------------
#### This repository has been created to reproduce a study
[![DOI](https://zenodo.org/badge/810518716.svg)](https://zenodo.org/doi/10.5281/zenodo.11508506)

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


Link: [https://media.springernature.com/full/springer-static/esm/art%3A10.1038%2Fs41586-024-07143-3/MediaObjects/41586_2024_7143_Fig14_ESM.jpg?as=webp](https://media.springernature.com/full/springer-static/esm/art%3A10.1038%2Fs41586-024-07143-3/MediaObjects/41586_2024_7143_Fig14_ESM.jpg?as=webp)

------------

### **Proposed workflow:**
| Steps | Explanation | Available links |
|-------| ------------| ----------|
| **1. Gather Data** |Load all the available datasets ||
||1. Antarctic Circumpolar Current strength record|[Link](https://doi.org/10.1038/s41586-024-07143-3)|
|  |2. Antarctic Ice Volume record| [Link](https://www.nature.com/articles/ncomms3999) |
||3. Asian Monsoon record|[Link](https://www.sciencedirect.com/science/article/pii/S0012821X10004425?casa_token=nPIDYsje-CwAAAAA:fHf6t0hC9bb7agt4cGz89tBGX5OxJmFdLmzy2SF-EWyOclaJfGSOQmwvCSUGOtx4esSxaEzBGaY)|
||4. Global Marine δ13C stack|[Link](https://www.science.org/doi/full/10.1126/science.aba6853?casa_token=2D6n76g8L1sAAAAA%3A9MFkaU13cOaZke17xRsSfrAyP1DCqGJ3htoOoKzm9sUqLr6_k4Yi4a7-30O_1hTMJchDgpBnvcBNXvk)|
||5. Eccentricity parameter|[Link](https://www.aanda.org/articles/aa/full/2004/46/aa1335/aa1335.html)|
| **2. Data Processing**| Process data for any missing values, interpolation to deal with unevenly spaced data etc. | [Data cleaning steps](https://pyleoclim-util.readthedocs.io/en/latest/core/api.html#pyleoclim.core.series.Series.clean) |
| **3. Spectral Analysis** | Perform spectral analysis on loaded series using pyleoclim package. | [Pyleoclim](https://pyleoclim-util.readthedocs.io/en/latest/)|
| **4. Filtering Timeseries**| Filter the timeseries for 413kyr periodicity.| [Filtering using pyleoclim](http://linked.earth/PyleoTutorials/notebooks/L1_filtering_and_detrending.html) |
| **5. Stackplot**| Create a stackplot combining all the timeseries to generate the final figure. | Function: [stackplot()](https://pyleoclim-util.readthedocs.io/en/v0.7.4/utils/plotting/stackplot.html) |

----------


## [**Link to the jupyter notebook**](https://github.com/PaleoPranay/pyRATES/blob/main/notebook/pyRATES_github.ipynb)


