# meli_test

Requests:

*python 3.6 or later is required with the following libraries:
  
          -flask
  
          -flask_restful
  
          -pandas
  
          -numpy
  
          -time
  
          -datetime

*PostMan

First step to run the API, is to run the notebook 'API.ipynb', you need to have the csv 'Experiments DataSet For Excercise-small.csv' in the same folder.

Next, you need to open PostMan, this is a really friendly app to make requests to API's. In this case, we are going to use the following ones:

GET https://host/experiment/<:id>/result?day=YYYY-MM-DD HH

GET https://host/experiment/results?day=YYYY-MM-DD HH

Where <:id> is the name of the experiment and day=YYYY-MM-DD HH the day with the the appropiate format to filter the csv.

The only problem is that if an experiment was used but none of its variants have sales, it will not be shown, instead of displaying 0 sales. This is something I have to keep working into.

Another important matter to consider, is that this is surely the first prototype of this API. In the future, the idea is to improve it using SPARK, with the library PySpark. This will increase the response time, since it is designed to work with bigdata.

