# Modeling Grocery Prices In Seven Countries  Using Bayesian Statistics
## Motivation
One of the advantages of being a Minerva Student is the opportunity to have quick access to fellow students from all around the world. This gives us a chance to broaden our horizons and apply our knowledge in various contexts and using a great variety of data. 

My model would help answer questions like: 
- To what extent do grocery prices vary by country and store brand? 
- Are grocery prices and the geographical distribution correlated with other cost-of-living measures?
I attempt to address these questions by utilizing Bayesian Statistics and PyStan functionality available in Python. Model setup, as well as conclusions, are described below. 
## About dataset
- total of 64 observations were collected during November 2020. The raw data included data from 7 countries, namely Germany, the United Kingdom, the United States of America, Morocco, Vietnam, South Korea, and Guatemala. Each country has from 2 (Guatemala, South Korea) to 22 (Germany) observations. There are 61 unique stores and 1 store with duplicate stores (located in San Francisco) in our dataset. 
- for the following products: apples, bananas, tomatoes, potatoes, flour, rice, milk, butter, eggs, chicken breasts
- pre-processing: 
  - A total of 34 observations had some missing values. The values were ‘missing at random’ (MAR), which implies that the propensity for a missing data point is related to some of the observed data, such as the type of the store (e.g. certain store did not have a lot of banana brands). It is often suggested to simply drop NAs; however, doing so would result in the deletion of 34 rows and is not suggested for such a small dataset and MAR. 
Given the above, I decided to replace some values with the mean value of the product. For computing the mean, I differentiated between the country, product, and store type. The algorithm for such mean computation is specified in notebook PART2. As a result, I obtained the following Table 1, which was used for replacing the missing values for the respective products in respective countries & stores. This was done manually using Google Sheets.
## Modeling
- the basic idea of the model is that each type of product has a base price, with multipliers depending on store brand and geographical location.
- 
## Results (for more, check ipynb)
![image](https://user-images.githubusercontent.com/44281687/121325045-f3685b00-c919-11eb-9fac-1dcb06c4a14a.png)
![image](https://user-images.githubusercontent.com/44281687/121325087-fc592c80-c919-11eb-825b-e1a69ee7d3d8.png)

## What is bayesian stats? 
![image](https://user-images.githubusercontent.com/44281687/128815425-725b30ea-54f2-48d9-b7b3-d2b54a6927f0.png)
