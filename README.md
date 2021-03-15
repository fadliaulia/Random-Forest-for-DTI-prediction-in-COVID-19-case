# Random-Forest-for-DTI-prediction-in-COVID-19-case

## Data
### Protein Data
The protein data used is the protein associated with COVID-19 in Human body. There are a total of 113 proteins on the OMIM and Uniprot sites and literature studies search results. There are 7 protein that related to COVID-19 in human body according to OMIM site, 28 COVID-19-related protein according to Uniprot, 19 COVID-19-related protein and 49 protein that has similar characteristics to ACE2 protein which protein that associated to COVID-19 according to Kuleshov et al., (2020). Kermali et al., (2020) also stated that there are 7 different proteins that has associations to COVID-19. In Zhang & Guo., (2020) and Chen et al., (2020) research, there is 1 protein each associated with COVID-19, whereas in the study of Coleman et al., (2016) there is 1 protein associated with the sars-cov virus. Total protein data used is 113 protein. Protein data can be accessed at proteincovidbaccession2.csv

### Drug-Target Interaction Data
Drug-Target Interaction Data were taken from SuperTarget and DrugBank sites. Of the 113 proteins, only 36 proteins have interactions with a compound on the DrugBank and SuperTarget sites. The searching process for compound-protein interaction data on the Drugbank site resulted in 786 interactions while the SuperTarget site resulted in 3415 interactions.

## DTI Prediction Model and Evaluation
Feature selection process with XGBoost algorithm reduce the data dimensions. Random undersampling on dataset is done by collecting all row data with positive interactions and randomly selects 20450 row data with unknown interactions. Model is then built using random forest algorithm. Another prediction models for DTI were also built using LGBM, GBM and XGBoost models to compare the results of random forest performance. All model is built using default parameter and evaluated using stratified K-fold cross validation with K=10. 

## Source code flow: Scraper Drug at Supertarget and Drug Bank.ipynb -> Merge Drugbank and Supertarget.ipynb -> Generate interaction and Feature Extraction Daming.ipynb -> Modeling Daming.ipynb

## References
Chen, X., Yin, Y. H., Zhang, M. Y., Liu, J. Y., Li, R., & Qu, Y. Q. 2020.  Investigating the mechanism of ShuFeng JieDu capsule for the treatment of novel Coronavirus pneumonia (COVID-19) based on network pharmacology. International Journal of Medical Sciences. 17(16): 2511-2530. doi: 10.7150/ijms.46378 &nbsp
Coleman, C. M., Sisk, J. M., Mingo, R. M., Nelson, E. A., White, J. M., & Frieman, M. B. (2016). Abelson Kinase Inhibitors Are Potent Inhibitors of Severe Acute Respiratory Syndrome Coronavirus and Middle East Respiratory Syndrome Coronavirus Fusion. Journal of virology, 90(19), 8924–8933. doi: 10.1128/JVI.01429-16 &nbsp
Kermali, M., Khalsa, R. K., Pillai, K., Ismail, Z., & Harky, A. (2020). The role of biomarkers in diagnosis of COVID-19 - A systematic review. Life sciences, 254, 117788. doi:10.1016/j.lfs.2020.117788 &nbsp
Kuleshov, M. V., Clarke, D., Kropiwnicki, E., Jagodnik, K. M., Bartal, A., Evangelista, J. E., Zhou, A., Ferguson, L. B., Lachmann, A., & Ma'ayan, A. (2020). The COVID-19 Gene and Drug Set Library. Research square, rs.3.rs-28582. doi:10.21203/rs.3.rs-28582/v1 &nbsp
Zhang, L., & Guo, H. (2020). Biomarkers of COVID-19 and technologies to combat SARS-CoV-2.   Advances in Biomarker Sciences and Technology 2:1-23. doi: 10.1016/j.abst.2020.08.001 &nbsp

