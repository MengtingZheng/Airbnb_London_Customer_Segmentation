This repository contains files for replicating the data analysis for the project "A Big Data Study on Behavioural Segmentation of Airbnb Users in the London Market".

This README file provides an overview of the replication materials for the project.

# Data
* This folder contains processed clean datasets that are ready to be fed into analysis. Raw data contain sensitive personal information of Airbnb guests and hosts so are not presented here for privacy reasons, but can be freely downloaded from the Inside Airbnb database: http://insideairbnb.com/get-the-data.html
* Six datasets can be found in the folder, each containing review data for one of Airbnb's listing types (shared room / private room / entire apartment/house) and one of the locations in London (inner London / outer London). The datasets are organised with the same structure, containing features including listing IDs, reviewer IDs, review IDs, dates of review, review texts, listing types and locations in London.

# Analysis
* `Clean_data.Rmd` replicates the process of cleaning the raw data to get the datasets in the Data folder.
* `Analyse_data_Function.Rmd` decontructs the steps within the self-written function `function_get_dfm.rds` that is called at the beginning of analysis to generate the document-feature matrix from a dataset.
* The remaining six files ending with `.Rmd` replicate the full analyses of the six datasets. They involve identical steps, including generating document-feature matrix, topic modelling, analysing the topic model and validating potential topics in the corpus with dictionary-based scaling.
* The remaining six files ending with `.rds` are the LDA models generated from the step of topic modelling for the six datasets. Since the LDA topic modelling algorithm takes a long time to run, the resulted models are saved as objects that can be quickly imported into the `.Rmd` files to perform further analysis.
