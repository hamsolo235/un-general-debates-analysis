# UN General Debates Analysis
An analysis of UN General Debate speeches in relation to military spending of member states.

## Motivation
This paper was written while I was studying towards an MSc in Public Policy at UCL, as required by the Advanced Quantitative Methods course undertaken in part completion of the degree.

## Data
The core data set, the UN General Debate corpus, from Mikhaylov et al. (2017), can be found here:<br>
Jankin Mikhaylov, Slava; Baturo, Alexander; Dasandi, Niheer, 2017, "United Nations General Debate Corpus", https://doi.org/10.7910/DVN/0TJX8Y, Harvard Dataverse, V5.
<br>
<br>
Military spending data was sourced from Bohmelt and Bove (2014):<br>
Böhmelt, Tobias, and Vincenzo Bove. 2014a. “Forecasting Military Expenditure.” Harvard Dataverse. https://doi:10.7910/DVN/24941.
<br>
<br>
The Correlates of War data set was used to provide control variables for regression models:<br>
Palmer, Glenn, Vito D’Orazio, Michael Kenwick, and Matthew Lane. 2015. “The Mid4 Data Set: Procedures, Coding Rules, and Description.” Conflict Management; Peace Science. http://cow.dss.ucdavis.edu/data-sets/ MIDs.
<br>
<br>
The sentiment lexicon published by Mohammad and Turney (2013) was used for the sentiment analysis component of the paper:<br>
Mohammad, Saif M., and Peter D. Turney. 2013. “Crowdsourcing a Word-Emotion Association Lexicon.” Computational Intelligence 29 (3): 436–65.
<br>

## Methodology and research design
The paper uses an LDA topic model to identify foreign policy and security related topics in the UN GD speeches between 1991 and 2001. The posterior document probablities were extracted from the model and used as weights applied to word counts of fear- and anger-related words as set out in Mohammad and Turney's (2013) sentiment lexicon. The resulting sentiment scores were used firstly in a panel linear regression model on military spending levels, and in a series of classification models (logistic regression, random forest and SVM) that attempted to classify a validation set of year-country pairs as demonstrating 'supernormal' military spending. 'Supernormal' was defined as being at least one standard deviation above the decade rolling average up to a given year.

## What's in the repository
I provide the original R markdown file (.Rmd), which contains my code and write-up, the rendered pdf that was submitted for the course, and other required files for knitting the markdown. The data sets are not included here but can be sourced using the references above in the 'Data' section. 


