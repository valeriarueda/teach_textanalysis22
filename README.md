# Text Analysys for Economists
**A hands-on introduction using R**

#

These are all the files needed for the graduate workshop on text analysis. Please refer to the syllabus in "docs" for more details.

## Lecture Materials

To read the lecture notes, open the link [notebook/MasterClass.ipynb](https://github.com/valeriarueda/teach_textanalysis22/blob/main/notebook/MasterClass.ipynb).


## Data Files
The data files are in the folder `data`

| Path|  Raw or Output| Description|
| -----| ----- | -----|
| "data/all_ECB_speeches.csv"|  Raw |  Data with all ECB speeches, downloaded [ECB website](https://www.ecb.europa.eu/press/key/html/downloads.en.html) |
| "data/all_ECB_speeches_20112022.csv" | Raw| ECB speeches from 2011 (since Mario Draghi's time) |
| "data/austen_chapters.csv" | Raw|  Corpus of Austen boks from `janeaustenr`, organised as one chapter per line |
| "data/docterm_ecb_austen.txt" | Raw|  document-term dataframe mixing the ECB and Austen corpus |
| "data/Loughran-McDonald_MasterDictionary_1993-2021.csv"  | Raw | Lougran and MacDocnald (2011) sentiment lexicon to be used with financial docs. Also available as an R package (lexicon_loughran in [textdata  library](https://emilhvitfeldt.github.io/textdata/index.html)) |
| "data/Loughran-McDonald_simplified.csv" | Raw | Lougran and MacDocnald (2011) sentiment lexicon simplified (with stems), for the purpose of this class only. It may be better to not use stemmed terms for sentiment analysis. |
| "data/open_pubs_2020-07_forclass.csv" | Raw | UK pub names and addressed, modified for the purpose of the class. Used to learn regular expressions.  [Original here](https://www.getthedata.com/open-pubs). |
| "data/output/speech_tfidf_20112022_wide.csv" | Output| TF-IDF matrix representation of ECB speeches since 2011. Wide format (one line per speech)|
|"data/output/speech_tfidf_20112022.csv" | Output|   TF-IDF matrix representation of ECB speeches since 2011. Long format (one line per stem $\times$ speech)|

## Materials
For this class, you need to have a working installation of R. To work with R, the IDEs RStudio or Jupyter will be useful. RStudio may be the easiest to sort out.

Make sure you have tested your version of R and basic commands, such as read.csv(), are running before the lecture. [This video](https://youtu.be/Eq8Xnueb-50) presents a tutorial on how to do load a dataset in R.

The following packages should be installed: `tidyverse`, `lubridate`, `reshape2`, `ggmap`, `sf`, `tidytext`, `stopwords`, `SnowBallC`, `glmnet`, `gamlr`, `topicmodels`, `textdata`, `ranger`.

To install a package, run the command: `install.package(“package”)`. For instance: `install.package(“tidyverse”)`.

In other words, the following header should run in your machine:

```
#General data handling
library(tidyverse)
library(lubridate)
library(reshape2)
#Maps
library(ggmap)
library(sf)
sf::sf_use_s2(FALSE) ## s2 in sf version 1.0 slows down the code too much
#Text analysis
library(tidytext)
library(stopwords)
library(SnowballC)
library(topicmodels)
library(textdata)
# ML 
library(ranger) #Random Forests
library(glmnet) #LASSO
library(gamlr) #LASSO choice lambda AIC

```
