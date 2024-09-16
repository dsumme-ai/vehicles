# Vehicles data set

Dataset contained 426,880 rows and 18 columns.

### Initial cleaning 'vehicles_df_dropped_na'  has 396,307 rows and 10 columns

Top 20 correlated Features 
![Screen Shot 2024-09-16 at 3 45 29 PM](https://github.com/user-attachments/assets/0265d036-19b3-4e45-b5db-8feeaba34102)
Strong Positive Correlations:

Fuel_gas and fuel_other (0.66): There seems to be a notable correlation between vehicles labeled as using "gas" and "other" fuels, which could indicate overlapping or misclassified categories.
Condition_good and condition_fair (0.55): This suggests that cars in "good" condition often tend to be closely related to those marked as "fair" condition, which could imply subjectivity in these classifications.
Manufacturer_tesla and fuel_electric (0.59): As expected, there’s a strong positive correlation between Tesla and electric vehicles.

Strong Negative Correlations:

Drive_fwd and drive_rwd (-0.43): There's a strong negative correlation between "front-wheel drive" (fwd) and "rear-wheel drive" (rwd), as these are mutually exclusive categories.
Fuel_electric and fuel_gas (-0.66): This reflects the natural exclusivity between electric and gas vehicles, as vehicles powered by gas are, by definition, not electric.
Fuel_hybrid and condition_good (-0.26): Interestingly, there’s a moderate negative correlation between hybrid vehicles and those in "good" condition, suggesting that hybrids might often be in different states of condition compared to non-hybrid vehicles.

Moderate to Weak Correlations:

Drive_rwd and type_pickup (-0.43): Rear-wheel drive vehicles tend to have a somewhat negative relationship with pickup trucks, which could reflect design differences where many pickup trucks are often four-wheel drive (4wd) or all-wheel drive (awd).
Manufacturer_ford and type_pickup (0.21): Ford is moderately associated with pickup trucks, which aligns with Ford’s strong brand presence in the pickup segment (e.g., Ford F-series).
Manufacturer_ram and type_pickup (0.23): Similarly, Ram is also moderately associated with pickup trucks.

Low or No Correlation:

Many features have low correlation values (close to 0), indicating that they are either independent or have very weak relationships with each other. For example, features like fuel_electric and type_sedan seem to have very little correlation.

Top 20 Postive positive correlated features with Price

![Screen Shot 2024-09-16 at 4 44 27 PM](https://github.com/user-attachments/assets/82df1b13-8dbc-461d-bc2a-bf49a1eb0a85)

All features with Price
![Screen Shot 2024-09-16 at 4 46 33 PM](https://github.com/user-attachments/assets/12384871-0504-436b-9faf-638a9c5f1edc)


# Model Performance

Random Forest is the best forming model

![Screen Shot 2024-09-16 at 3 50 33 PM](https://github.com/user-attachments/assets/933083c0-edd7-4186-9e9f-e5441ba2a79f)

Model vs Actual data

![Screen Shot 2024-09-16 at 3 53 10 PM](https://github.com/user-attachments/assets/b8d968b1-6e08-42ce-b40f-74210737c3f4)



# Final Recommendations for the Dealership:
* Select inventory that consumers value the most, such as low mileage and recent manufacturing year. Based on feature importance and correlation analysis, these factors heavily influence price.

* Focus inventory on vehicles that have higher predicted prices (e.g.,  Pickups, Hybrid cars  and electric from well-known manufacturers like Tesla).

* Be cautious about overpricing older vehicles or those with higher mileage, as they have a negative impact on resale value.

The graphs above, gives a foundation to a dealerships to understand both the factors affecting car prices and how they can optimize their inventory and pricing strategy based on consumer preferences. As well has how the model was choosen

#  Next steps and recommendations

1. Conduct deeper Exploratory Data Analysis (EDA)
2. Explore feature engineering (handle additional outliers)
3. Perform Principal Component Analysis (PCA) to reduce dimensionality and analyze the broader dataset of 3M records.

