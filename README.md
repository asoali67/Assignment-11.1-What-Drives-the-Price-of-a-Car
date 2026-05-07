# Assignment-11.1-What-Drives-the-Price-of-a-Car

From using two different modeling i have found two set of features that has the most effect of the price of a car

1. First modeling is to use SequentialFeatureSelector with LinearRegression , the result of the model suggested the following featurs drive the car price the most as bellow

|title_status        | state     |cylinders    |transmission    | manufacturer       |condition|
| :---               | :---:     | :---:        | :---:         | :---:                |---: |
|0 -16584.886352 |-16371.837798  |8740.44308   |10204.210126    | 11882.745145     | 14977.541527 |

And that title_status and condition is the features that have the biggest effect on the price


2. Second modeling i used Lasso with GridSearchCV and k-fold = 5 , the result was different as it identified odometer and year of the car the two features that have the most effect. one thing to note i was expecting the odometer to have a negative value as the odometer goes up the price of the car would go down 

     | year         | fuel       | paint_color    |  type       | state       | transmission     | title_status   | condition        | drive     |  odometer  |
      | :---        | :---:       | :---:          | :---:      | :---:       | :---:            |     :---:      |       :---:      | :---:      |---: |
|0 -43804.023861 |-30850.243117 |-19208.254532 |-12571.838364 |-7331.577452   |-2317.822403       |-97.570254     | 7525.611279   |23344.583248  |122667.319441  |


Nwverthe less with the result i have i would recomend to take the 4 feaurs from both models as the biggest factors of the price of a car and they are 
year, odometer, title_status and condition

While cleaning the data i removed the model feature from the dataset, the data did not have data integrety and same model of car was identified with different names. i think it is was better for me to fix that feature and include it in the dataset for anylysis, But the time was short to to such work.

I would also like to try different encoding techniques to see what effect has on the feature selection result. 
