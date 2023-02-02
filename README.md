# About
The project was about streaming real-time tweets mentioning earthquake all aorund the world to train a model where it distinguishes real earthquake tweets from fake one with help of NLP model. 

# How
Real-time tweets are streamed through Twitter V.2 API into local socket from which the data is being read by Spark client. Spark client write stream-data as batch into Azure Cosmos DB to store raw data (to keep raw data for further analysis). 
Raw data is cleaned and preprocessed before being fed into ML model. Then, ML model takes tweets and classify it as real or fake alert. 

# Run 
All tasks (getting tweets, reading them with Spark, processing data) take place in a separate Docker container. All you need to do is to run docker compose which in turn creates docker images and spin docker containers. 
