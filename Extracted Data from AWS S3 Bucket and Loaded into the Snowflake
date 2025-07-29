CREATE WAREHOUSE YELP_WH
WITH
    WAREHOUSE_SIZE = 'Large'
    WAREHOUSE_TYPE = 'STANDARD'
    AUTO_SUSPEND = 60
    AUTO_RESUME = TRUE
    INITIALLY_SUSPENDED = TRUE;

create database YELP_DB;
create schema YELP_DB.YELP_SCHEMA;
create stage YELP_DB.YELP_SCHEMA.YELP_STAGE;
list @yelp_stage;
alter warehouse YELP_WH Set 
warehouse_size = 'X-Large';
drop stage if exists
YELP_DB.YELP_SCHEMA.YELP_STAGE;

CREATE or replace table yelp_db.yelp_schema.yelp_reviews (review_text variant);

copy into yelp_reviews
from 's3://copy path which re-directs to your S3 Bucket'
credentials = (
    AWS_KEY_ID = 'Your AWS User Key'
    AWS_SECRET_KEY = 'your Secret Key'
)
FILE_FORMAT = (TYPE = JSON);

SELECT * FROM YELP_REVIEWS;

CREATE OR REPLACE TABLE YELP_DB.YELP_SCHEMA.YELP_BUSINESSES (business_text variant);

copy into YELP_BUSINESSES
from 's3://copy path which re-directs to your S3 Bucket'
credentials = (
    AWS_KEY_ID = 'Your AWS User Key'
    AWS_SECRET_KEY = 'your Secret Key'
)
FILE_FORMAT = (TYPE = JSON);

SELECT * FROM YELP_BUSINESSES;