# UT-DS-KNIME-Advanced
Data Science with KNIME (Advanced) course - University of Tehran
-----------------------------------------------------
Review Assignment 1: Complete this assignment by Mehr 6, 12 PM.

Task 1: Read cars-85.xlsx including only the following columns: make, fuel_type, cylinders_nr, horse_power, city_mpg, highway_mpg and price.

Task 2: Exclude the cars which their "make" value is "jaguar".

Task 3: Handle the missing values by inputing the rounded average for horse_power and removing the whole row for other columns.

Task 4: Convert cylinder_nr from string numbers to digits.

Task 5: Create a new column named "engine" which contains the values of horse_power, cylinder_nr and fuel_type. Seperate values by an underscore and use uppercased fuel_type.

Task 6: Create a new column which contains the difference between each car's price and the average price of all cars.

Task 7: For each "make" value (which is the brand) show the average of price difference (produced in task 6) and the mode of "engine" (produced in task 5).

-----------------------------------------------------
Review Assignment 2: Complete this assignment by Mehr 16, 12 PM.

Task 1: After task 3 in last assignment, calculate the average mpg (city and highway) for each car.

Task 2: Normalize price and average mpg by Min-Max normalization. Set min to 0 and max to 1.

Task 3: Use K-Means for clustering based on price and average mpg. Set number of clusters to 4.

Task 4: Denormalize price and average mpg using the normalization model built in task 2.

Task 5: Join "body-style" and "drive-wheels" columns from the original dataset (the output of task 1 in review assignment 1) to the current set based on row IDs.

Task 6: Assign different colors to each cluster.

Task 7: Use a scatter plot to visualize data on price and average mpg. In the cluster that contains cars with the highest average mpg, select 3 cars which are a bit seperated from the others and have the highest average mpg values.

Task 8: Filter out the selected cars in the previous task.

Task 9: Filter out the column created in task 7.

Task 10: Devide the dataset into 2 parts (4:1).

Task 11: Use Desicion Tree and Naive Bayes to train 2 classification models (use clusters as classes) and evaluate both of them.

-----------------------------------------------------
Main Assignment 1: To complete this assignment you need to download a json file from this link: http://bulk.openweathermap.org/sample/city.list.json.gz which contains the list of cities and their IDs at openweathermap.org; You are going to use the website's api to collect weather information of selected cities.

Part 1: In this part you are going to prepare a list of cities in Iran and their IDs:

Task 1: Unzip the gz file and move the json file to you workspace and then read the file in KNIME using JSON Reader node.

Task 2: Use JSON Path or XPath (you can use XPath after converting JSON to XML) to get IDs, names and countries from the file.

Task 3: Exclude any other columns than those 3 new columns from task 2.

Task 4: Filter the dataset to keep the records which their country is Iran (IR). As you may see, there are duplicates in cities. Use a GroupBy node and use cities as group column and use "First" or "last" aggregation for IDs. (Countries are not required anymore)

Task 5: Use a Table Row To Variable Loop Start to feed the IDs to the next part of your workflow.

Part 2: In this part you are going to loop over a get request to openweathermap.org and collect the weather information of the cities you have selelcted already:

Task 6: Go to openweathermap.org and read the API documentation of the website and collect the current weather info of the cities you have selected by city IDs.

Additional Task: Find the states that each city belongs to and then show the mode of weather status for each state.
