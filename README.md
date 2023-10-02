# YouTube-analysis
## Goals of the Project
1. Data Ingestion
2. ETL Design
3. Data Lake: To easily organise the data and build a data pipeline around it.
4. Scalability
5. AWS Cloud
6. Reporting

## Major Elements of the Project
1. Build Data lake from scratch in Amazon S3
2. How to build a data lake
3. Differences between Data Lake and Data warehouse
4. How to design a Data Lake and how to properly partition tables
5. AWS Data Catalog - How to use Glue for Cataloging?
6. ETL in AWS spark
7. AWS SNS
8. SQL using Amazon Athena and Spark SQL
9. Script to ingest data incrementally
10. Build a Dash board.

S3 bucket:  
bhavana-project  
Gnapikaaws@123  
Access Key:AKIAQMMFWHUDWLJGN2C6  
Secret Access Key: 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

### Steps:
1. aws configure  
2. aws s3 ls (to list s3 buckets)  
3. Copy files from local to S3  
   aws s3 cp . s3://datae-on-youtube-raw-useast1-dev/youtube/raw_statistics_reference_data/ --recursive --exclude "*" --include "*.json" 
4. Copy csv files into respective folders    
    aws s3 cp CAvideos.csv s3://datae-on-youtube-raw-useast1-dev/youtube/raw_statistics/region=ca/  
    aws s3 cp DEvideos.csv s3://datae-on-youtube-raw-useast1-dev/youtube/raw_statistics/region=de/  
    aws s3 cp FRvideos.csv s3://datae-on-youtube-raw-useast1-dev/youtube/raw_statistics/region=fr/  
    aws s3 cp GBvideos.csv s3://datae-on-youtube-raw-useast1-dev/youtube/raw_statistics/region=gb/  
    aws s3 cp INvideos.csv s3://datae-on-youtube-raw-useast1-dev/youtube/raw_statistics/region=in/  
    aws s3 cp JPvideos.csv s3://datae-on-youtube-raw-useast1-dev/youtube/raw_statistics/region=jp/  
    aws s3 cp KRvideos.csv s3://datae-on-youtube-raw-useast1-dev/youtube/raw_statistics/region=kr/  
    aws s3 cp MXvideos.csv s3://datae-on-youtube-raw-useast1-dev/youtube/raw_statistics/region=mx/  
    aws s3 cp RUvideos.csv s3://datae-on-youtube-raw-useast1-dev/youtube/raw_statistics/region=ru/  
    aws s3 cp USvideos.csv s3://datae-on-youtube-raw-useast1-dev/youtube/raw_statistics/region=us/  
5. Create AWS Data Lake: Where we store everthing structures and semistructured data with which we can build a data warehouse.
6. Create AWS Glue Catalog : Info about the data and what it contains.
   !<img width="818" alt="Screenshot 2023-09-21 at 9 41 10 PM" src="https://github.com/itsmeBhavana/YouTube-analysis/assets/3799601
    1/a89ab0d2-7e55-43c1-aa06-20b8a508d3bc">  
   !<img width="838" alt="Screenshot 2023-09-21 at 9 42 31 PM" src="https://github.com/itsmeBhavana/YouTube-analysis/assets/37996011/6064c3ca-493d-41f7-8e53-125d474f0ebe">
7. Open with Athena Tables. Athena is an Adhoc query tool that is used to query SQL.
8. Run Lambda function to do the preprocessing i.e to convert from
9. Do the ETL upon the cleansed data using Glue ETL Jobs.
10. Extract the data from the raw bucket
11. Transformations-change schema
12. All the data types are converted into strings. Manually unchange them to boolean and bigint.
13. Spark file is created.
14. Edit the spark file
15. The output data will be available in a single file.
16. So, we need to do some optimizations in the code so as to represent the region wise partitions like in the input folder.
17. Add a partition key that is Region
18. 

   
   
