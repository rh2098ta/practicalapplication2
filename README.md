Module 11: Practical Application 2: What Drives the Price of a Car? 

[Open the Jupyter Notebook on GitHub → practicalapplication2.ipynb](https://github.com/rh2098ta/practicalapplication2/blob/main/practicalassignment2.ipynb)

Datasource: Kaggle

For this assignment, I needed to figure out what actually drives the price of a used car and turn that into something a dealer/dealershiop could use when deciding what vehicles to buy and how to price them. I worked with a large dataset of used car listings (including 3 million used cars) and followed the CRISP-DM process (after reading the two documents assigned). The CRISP-DM process helped me start with the business problem, understand the data, clean it, test different models, and then translate the results back into plain English for the people who would actually use them.

The first step was reviewing the data and cleaning it up. There were a lot of missing values (NaN), unrealistic prices, and other things that needed to be filtered out before modeling. After cleaning the dataset and keeping only the most useful features, including fuel type, brand, mileage, and vehicle age, I trained several models to estimate car prices.

<img width="1000" height="688" alt="image" src="https://github.com/user-attachments/assets/83e80011-b85c-4660-a3e3-747def4a8b53" />


I started with linear regression as a baseline, and it was able to predict used car prices with a mean absolute error (MAE) of about $5,458 and an RMSE of about $7,290. That gave me a decent starting point, but the error was still high, so I moved on to a nonlinear model: Random Forest. After testing the model with cross-validation and doing a lightweight grid search to tune tree count, the Random Forest dropped the error to about $4,608 MAE and $6,296 RMSE. That means the Random Forest was around $850 more accurate per vehicle compared to linear regression, which is a meaningful difference for a dealership working with thousands of cars.



Once I had the best model, I looked at which features had the strongest effects on price. Trucks, diesel engines, and certain brands like GMC, RAM, and Ford showed up as some of the biggest price boosters, adding between $1,000 and $4,500 on average depending on the feature. Paint color even mattered more than I expected, with white and black cars pricing higher than others. On the low-end side, sedans were the biggest value drop, reducing price by about $5,700 on average. 

<img width="1394" height="828" alt="image" src="https://github.com/user-attachments/assets/44792d1f-97be-41ae-adf6-38123c69b368" />


Gas-only vehicles, small hatchbacks, and economy brands like Honda, Kia, Hyundai, and Nissan were also consistently cheaper in the market based on the model’s coefficients.

<img width="1100" height="702" alt="image" src="https://github.com/user-attachments/assets/a08f4116-5007-4122-96e5-390ff728cde3" />


Looking back at CRISP-DM, the phases actually lined up well with what I did. The business understanding phase made me define success not as “build the most accurate model possible” but “give a dealership information that changes how they buy and price cars.” Data understanding and preparation took the most time, as expected, because real datasets never start out clean. Modeling and evaluation were where I actually saw the trade-offs between simple, explainable models and more accurate but complex ones. The final “deployment” stage in this case doesn’t mean software — it just means delivering the results in a way a non-technical audience can understand and use.

Overall, the main takeaway from the analysis is that vehicle type, fuel type, and brand matter a lot more than things like mileage alone. Trucks and diesel vehicles are pricing strong, while sedans and small gas cars clearly depreciate faster. The tuned Random Forest model is accurate enough to support pricing decisions within a few thousand dollars, which is acceptable in a market where prices can range from under $5,000 to over $50,000. If I were actually handing this off to a dealership, the recommendation would be to stock more diesel trucks and fewer sedans if the goal is to maximize resale value.
