# Equivalent Pharmaceutical ID
The Equivalent Pharmaceutical ID (EPID) is a system used to group related pharmaceutical products together and provide a normalized system for naming. The EPID is intended to be used in healthcare applications to allow regional medication databases to be normalized to a non-branded/trade name product.

## Data Sources
The current version of the EPID is constructed from Canadian data, but is intended to use more international sources as time allows. Specifically, it is utilizing the following data sources to construct the EPID database:
- [Health Canada Drug Product Database Data Extracts](https://www.canada.ca/en/health-canada/services/drugs-health-products/drug-products/drug-product-database/what-data-extract-drug-product-database.html)
These data sources are used to assemble a comprehensive list of possible pharmaceutical products, which is then reviewed for any possible additions to the EPID.

## The EPID List
The list provides a unique EPID with a single product name (composed of the active ingredients, strengths, and unique pharmacokinetic parameters). Dosage forms are not included as different forms may still be considered equivalent (e.g. tablets and capsules).

## Reference Lists
This repository contains reference lists to link the EPID to other available pharmaceutical databases. The following references are available/planned:
- [Health Canada Drug Product Database Data Extracts](https://www.canada.ca/en/health-canada/services/drugs-health-products/drug-products/drug-product-database/what-data-extract-drug-product-database.html): *EPID* to *DRUG_CODE* and *EPID* to *DIN* - ***IN DEVELOPMENT***
- [Non-Insured Health Benefits Drug Benefit List](https://www.canada.ca/en/health-canada/services/publications/health-system-services/non-insured-health-benefits-drug-benefit-list.html): *EPID* to *DIN/PIN/NPN* - ***IN DEVELOPMENT***
- [Alberta Blue Cross Interactive Drug Benefit List](https://idbl.ab.bluecross.ca/idbl/load.do): *EPID* to *productID* - ***IN DEVELOPMENT***
- [Alberta Blue Cross Drug Price List](https://www.ab.bluecross.ca/providers/pharmacy-price-files.php): *EPID* to *DIN/PIN/NPN* - ***IN DEVELOPMENT***
- Albert Netcare Pharmaceutical Information Network: *EPID* to *Medication Name/Strength/Dosage Form* - ***IN DEVELOPMENT***
