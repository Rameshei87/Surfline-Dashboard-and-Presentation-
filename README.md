# Surfline-Dashboard-and-Presentation-

Architecture

![image](https://user-images.githubusercontent.com/110036451/184506268-0948c9ff-5f45-460e-a1dc-4d996675e2eb.png)


Surfline App Architecture

Overview

The pipeline collects data from the surfline API and exports a csv file to S3. Then the most recent file in S3 is downloaded to be ingested into the Postgres datawarehouse. A temp table is created and then the unique rows are inserted into the data tables. Airflow is used for orchestration and hosted locally with docker-compose and mysql. Postgres is also running locally in a docker container. The data dashboard is run locally with ploty.

ETL


![image](https://user-images.githubusercontent.com/110036451/184506276-7e2a01dc-8152-4d51-ab1b-3b581b712b4f.png)


Data Warehouse - Postgres


![image](https://user-images.githubusercontent.com/110036451/184506292-ca33a00c-96f9-442d-b183-3479bf024faa.png)



Data Dashboard

![image](https://user-images.githubusercontent.com/110036451/184506303-943f975c-9bd5-44e6-9dad-f98b945bc692.png)
