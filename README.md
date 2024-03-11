## Objective
My goal is to build an EPS database which stores analysts forecasts and real EPS for the companies in the following TICKER_LIST :
TICKER_LIST={AMZN, AAPL, MSFT, GOOG, TSLA, JNJ, PG, NVDA, CSCO, BABA, HD,BIDU, WMT, CRM, LULU, TGT, PANW, ADBE, VMW, MU, NKE, ORCL, BB, HPQ, COST, AMAT,BAC, CVX, AMGN, PG}.

Estimize is designed to collect opinions from the widest possible range of contributors, while maintaining the highest quality data through advanced behavioral and statistical algorithms.


#### Features include
* Contribute anonymously
* Give-to-Get
* Quality control and smart consensus
* Alerts, screening, Excel files

#### Creating Schemas
First, we created a file that will be used to connect to the database and perform the necessary DB operations such as create the database, create the tables, and drop all ahead of time to start fresh. Our code included the following steps:
* Create a connection object
* Drop database ESTIMIZE DB 
* Create the ESTIMIZE DB if not exists
* Drop all tables in the DB and get ready for a fresh start

After that, we created tables for each of the following:
* Company info (company_info)
* Company info  (eps_info)
* Analyst info (eps_analyst_info)
<img width="1817" alt="image" src="https://github.com/TiffanyWilkins/Data-Management-for-Analytics-Project/assets/54362628/d7103e53-2eae-4108-ad87-82301a3e199f">















