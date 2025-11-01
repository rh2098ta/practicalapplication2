Module 11: Practical Application 2: What Drives the Price of a Car? 
[Open Notebook on GitHub](https://github.com/rh2098ta/practicalapplication2/blob/main/practicalapplication2.ipynb)
Datasource: Kaggle

For this assignment, the goal was to figure out what makes some used cars worth more than others. I worked with the vehicles.csv dataset, which has millions of used car listings, and built a model to predict price based on things like vehicle type, fuel type, manufacturer, transmission, and mileage. I also followed the CRISP-DM (from the two documents assigned for this exceerise) process instead prior to my coding in GoogleCollab. The CRISP-DM forces you to think about the actual business problem first and for this assignment, helping used car dealers decide what kinds of cars are worth buying and reselling. I then was able to go step by step through understanding the data, cleaning it, building the model, and checking if the results make sense in real life.

After cleaning up bad data (like missing prices or extreme outliers), I trained a regression model and got an average error of around $6,000 per car (MAE). That sounds high at first, but this dataset includes everything from old cheap cars to high-end trucks, so that level of error is expected and still good enough to spot real pricing patterns.

Here’s what I found:

Trucks, pickups, and diesel cars sell for more — usually $3,500 to $4,500 above baseline. Regaring brands, American brands like GMC, RAM, and Ford also hold value better, adding about $1,000–$1,300. Through the analysis of the data, paint color mattered as well, such as white and black cars being priced higher on average. Types of cars mattered as well, including sedans and hatchbacks which were worth a lot less, with sedans dropping about $5,700. WHen comparing gas vs. diseal, analysis indicated that gas-cars were cheaper. With regards to deprecaition, brans such as Honda, Kia, Hyndai, and Nissan depreciated more than the tohers. 

Using CRISP-DM -- 

Business Understanding: Defined the real goal — help dealers make smarter buying decisions.
Data Understanding: Explored the raw dataset and noticed missing and unrealistic values.
Data Preparation: Cleaned the data, removed bad rows, fixed price and mileage issues, and selected useful features.
Modeling: Trained a regression model that predicts car prices based on the selected variables.
Evaluation: Focused on the meaning of numbers for a dealership vs. just reporting metrics (output from the code).
Deployment: Turned the results into practical recommendations

Key Findings for Dealers: 

Based on the model’s results, the types of cars that hold the most value are diesel trucks and pickups, especially those from American brands like GMC, RAM, and Ford. These vehicles consistently showed the highest resale prices, and even details like paint color made a difference, with white and black vehicles selling for more on average. In contrast, sedans, hatchbacks, and gas-only cars tended to lose value much faster, especially those from manufacturers such as Honda, Kia, Hyundai, and Nissan. If a dealer wants to maximize profit, the data suggests prioritizing trucks and diesel vehicles in their inventory, while treating sedans and small gas-based cars as low-margin purchases that only make sense at a steep discount.
