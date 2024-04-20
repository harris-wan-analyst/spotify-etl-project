# Spotify AWS ETL Project (End to End Data Pipeline) 
(Credit: Darshil Parmar)

## Architecture Diagram
<img width="719" alt="Screenshot 2024-04-13 at 9 39 43 PM" src="https://github.com/harris-wan-analyst/spotify-etl-project/assets/117702329/f0acd457-6c28-428f-bcac-c3bcd862b194">

## Project Details 
### Objective: 
- Develop an automated ETL pipeline using Python and AWS to obtain Spotify "Top Songs - Global" on weekly basis
### 3 Phases (Extract / Transform / Load)
1. Extract (Retrieve data from various sources)
   - Extract data through Spotify API
   - Deploy python codes for data extraction in AWS Lambda
   - Set trigger in CloudWatch to run weekly
   - Data stored in S3 Bucket
  
2. Transform (Convert messy data into useful formats)
   - Deploy python codes for data transformation in AWS Lambda
   - Set S3 trigger to run when new data is added
   - Transformed data is separated into 3 folders (Album / Artist / Song)
  
3. Load (Moves transformed data into repository)
   - AWS Glue Crawler will automatically infers data schema
   - AWS Glue Data Catalog serves as the metadata repository (e.g. column names / number of rows)
   - Query like SQL using AWS Athena

