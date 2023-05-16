# FOIA_COA_2022
## Excel/Google Sheets Analysis of COA USPS requests

This is an analysis of COA (Change of Address) requests made to the USPS (United States Postal Service) during the year of 2022. 
In this analysis we attempt to answer two questions primarily, and we explore two questions secondarily. Namely: we are curious about the which zip codes had the most people moving to them, and which had the most moving away from them. After we answer these questions, we briefly explore the same format questions, but with regards to states.

This analysis could be useful to real-estate agents and business development analysts who are seeking where to expand to next.

## Data Acquisition and Analysis

Initially we downloaded the file from [usps website](https://about.usps.com/who/legal/foia/documents/change-of-address-stats/Y2022.csv). After uploading to google sheets, we evaluated the data and [USPS's documentation](https://about.usps.com/who/legal/foia/documents/change-of-address-stats/coa-stats-explanation.pdf) to understand how we could best understand the question. First we note that our interest is in individuals' COA requests and not businesses. Second we note that we are interested in permanent residential changes, i.e., we want to know where people are settling and not where they are temporarily staying for reasons other than long-term residential plans. Thusly we know that we are interested in three columns primarily: ZIPCODE, and the two TOTAL PERM columns. We are interested in both columns for two reasons: 1) we do not want to over-cound people who are moving within the same zipcode as people who are moving to the zipcode freshly 2) We want to show growth within a community and not necessarily an equal exchange of residents. If the same number of people moving into a zipcode are also moving out of a zipcode, then there is no obvious growth potential for businesses, though there may be some for real estate agents.

We can now discern a formula from which we can calculate the approximate growth in a zip code by COA requests: 
$$left \sum_k=1^12 c_k - b_k = Z_i \forall i \in ZIPCODES.
