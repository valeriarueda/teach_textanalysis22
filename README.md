# Teaching Text Analysys for Economists
## A hands-on introduction using R

These are all the files needed for Valeria's text analysis class. Please refer to the syllabus in "docs" for more details.

## Lecture materials

To read the lecture notes, open the link [notebook/MasterClass.ipynb](https://github.com/valeriarueda/teach_textanalysis22/blob/main/notebook/MasterClass.ipynb).


## Data Files
The data files are in the folder `data`

| Path|  Raw or Output| Description|
| -----| ----- | -----|
| "data/all_ECB_speeches.csv"|  Raw |  Data with all ECB speeches, downloaded [ECB website](https://www.ecb.europa.eu/press/key/html/downloads.en.html) |
| "data/all_ECB_speeches_20112022.csv" | Raw| ECB speeches from 2011 (since Mario Draghi's time) |
| "data/Loughran-McDonald_MasterDictionary_1993-2021.csv"  | Raw | Lougran and MacDocnald (2011) sentiment lexicon to be used with financial docs. Also available as an R package (lexicon_loughran in [textdata  library](https://emilhvitfeldt.github.io/textdata/index.html)) |
| "data/Loughran-McDonald_simplified.csv" | Raw | Lougran and MacDocnald (2011) sentiment lexicon simplified (with stems), for the purpose of this class only. It may be better to not use stemmed terms for sentiment analysis. |
| "data/open_pubs_2020-07_forclass.csv" | Raw | Description|
| "data/output/speech_tfidf_20112022_wide.csv" | Output| TF-IDF matrix representation of ECB speeches since 2011. Wide format (one line per speech)|
|"data/output/speech_tfidf_20112022.csv" | Output|   TF-IDF matrix representation of ECB speeches since 2011. Long format (one line per stem $\times$ speech)|
