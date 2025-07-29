CREATE OR REPLACE TABLE tbl_yelp_reviews as
SELECT review_text:business_id::string as business_id,
review_text:date::date as review_date,
review_text:user_id::string as user_id,
review_text:stars::number as review_stars,
review_text:text::string as review_text,
analyze_sentiment(review_text) as sentiments
FROM YELP_REVIEWS;

SELECT * FROM tbl_yelp_reviews;

CREATE OR REPLACE TABLE tbl_yelp_businesses as
SELECT business_text:business_id::string as business_id,
business_text:name::string as name,
business_text:city::string as city,
business_text:state::string as state,
business_text:review_count::string as review_count,
business_text:stars::number as stars,
business_text:categories::string as categories
FROM YELP_BUSINESSES;

select * from tbl_yelp_businesses;