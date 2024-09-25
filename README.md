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
|||1. Antarctic Circumpolar Current strength record|[Link](https://doi.org/10.1038/s41586-024-07143-3)|
|  |2. Antarctic Ice Volume record| [Link](http://scholar.google.com/scholar_lookup?&title=Persistent%20400%2C000-year%20variability%20of%20Antarctic%20ice%20volume%20and%20the%20carbon%20cycle%20is%20revealed%20throughout%20the%20Plio-Pleistocene&journal=Nat.%20Commun.&doi=10.1038%2Fncomms3999&volume=5&publication_year=2014&author=de%20Boer%2CB&author=Lourens%2CLJ&author=Wal%2CRSW) |
||3. Asian Monsoon record|[Link](http://scholar.google.com/scholar_lookup?&title=Seven%20million%20years%20of%20wind%20and%20precipitation%20variability%20on%20the%20Chinese%20Loess%20Plateau&journal=Earth%20Planet.%20Sci.%20Lett.&doi=10.1016%2Fj.epsl.2010.07.004&volume=297&pages=525-535&publication_year=2010&author=Sun%2CYB&author=An%2CZS&author=Clemens%2CSC&author=Bloemendal%2CJ&author=Vandenberghe%2CJ)|
||4. Global Marine δ13C stack|[Link](http://scholar.google.com/scholar_lookup?&title=An%20astronomically%20dated%20record%20of%20Earth’s%20climate%20and%20its%20predictability%20over%20the%20last%2066%20million%20years&journal=Science&doi=10.1126%2Fscience.aba6853&volume=369&pages=1383-1387&publication_year=2020&author=Westerhold%2CT)|
||5. Eccentricity parameter|[Link](https://www.aanda.org/articles/aa/full/2004/46/aa1335/aa1335.html)|
| **2. Data Processing**| Process data for any missing values, interpolation to deal with unevenly spaced data etc. | [Data cleaning steps](https://pyleoclim-util.readthedocs.io/en/latest/core/api.html#pyleoclim.core.series.Series.clean) |
| **3. Spectral Analysis** | Perform spectral analysis on loaded series using pyleoclim package. | [Pyleoclim](https://pyleoclim-util.readthedocs.io/en/latest/)|
| **4. Filtering Timeseries**| Filter the timeseries for 413kyr periodicity.| [Filtering using pyleoclim](http://linked.earth/PyleoTutorials/notebooks/L1_filtering_and_detrending.html) |
| **5. Stackplot**| Create a stackplot combining all the timeseries to generate the final figure. | Function: [stackplot()](https://pyleoclim-util.readthedocs.io/en/v0.7.4/utils/plotting/stackplot.html) |

----------


[**Link to the jupyter notebook**](https://github.com/PaleoPranay/pyRATES/blob/main/notebook/pyRATES_github.ipynb)







