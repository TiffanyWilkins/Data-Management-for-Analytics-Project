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

``` import pymysql
#Create a connection object
conn = pyml.connect(host='127.0.0.1', port=3306, user='', passwd='',autocommit=True)
cur = conn.cursor()

# Drop database ESTIMIZE DB
cur.execute("DROP DATABASE IF EXISTS msa_estimize_db")

# Create the ESTIMIZE DB if not exists
cur.execute("DROP TABLE IF EXISTS msa_estimize_db.company_info")
cur.execute("DROP TABLE IF EXISTS msa_estimize_db.eps_info")
cur.execute("DROP TABLE IF EXISTS msa_estimize_db.eps_analyst_info")
cur.execute("DROP TABLE IF EXISTS msa_estimize_db.analyst_info")

# Create a table for Company Information: company_info
cur.execute("CREATE TABLE IF NOT EXISTS msa_estimize_db.company_info (\
c_id INT UNIQUE NOT NULL AUTO_INCREMENT,\
ticker VARCHAR(25) NOT NULL,\
company_name VARCHAR(100) NOT NULL,\
sectors VARCHAR(200) NOT  NULL,\
industries VARCHAR(200) NOT NULL,\
followers INT NOT NULL,\
analysts INT NOT NULL,\
PRIMARY KEY (c_id))\)
```

#### DATASCRAPPING

<img width="956" alt="image" src="https://github.com/TiffanyWilkins/Data-Management-for-Analytics-Project/assets/54362628/2ad2dfee-a23f-4931-bc49-a38484b462ba">

### Main Steps:
* Get a random values for light sleep and heavy sleep
* Login to the Estimize Website via Selenium
* Loop through the ticker list and pull the company info
* Loop through the ticker list and pull the EPS Table info
* Loop through the ticker list and the quarter list and
          pull the eps analyst data
<img width="492" alt="image" src="https://github.com/TiffanyWilkins/Data-Management-for-Analytics-Project/assets/54362628/0f6e84bc-cec4-4fd1-b47a-32400d2f7b87">





















