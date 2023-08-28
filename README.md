# BeerBelly Web Application

Web application written in Python using `flask` and deployed on Heroku. 
Sample hosted on Heroku:
https://beerbellyapp-62abfa954241.herokuapp.com/

1. Data Preparation: Source of data from https://data.world/socialmediadata/beeradvocate/
   
2. Data processing: Duplicated entries were removed & the reviews by the customers were processed using NLP & rule-based filtering. A total of 5 different ratings were identify to be used as input features. 

3. Modeling: Matrix Factorization (ALS) was used & user-rating matrix was generated. Model was ran using PySpark.
   
4. Deployment: We stored the result of the model in AWS S3 & utilize AWS Lambda as a trigger to push the newly generated result into AWS DynamoDB.

5. FLASK FRONT END: This python flask front end will then able to call the API from AWS DynamoDB and return the top 10 recommendations.

   (Note: This web app has depreciated due to the AWS DynamoDB API has been shutdown)
