Test plan
# High level test plan

|Test ID|Description|Expected I/P|Expected O/P|Actual O/P|Type of Test|
| :- | :- | :- | :- | :- | :- |
|H\_01|Check if stock dataframe is created or not|Stock name|Dataframe|PASS|Requirement based|
|H\_01\_01|Check dataframe initialized from csv|(1)File name |Dataframe initialized from csv|PASS|Scenario/technical|
|H\_02|Check for NaN or missing values in dataframe|Dataframe|Dataframe without NULL or NaN values|SUCCESS|Requirement based|
|H\_02\_02|Check if dataframe has all the historical data|Dataframe|Dataframe with all the historical data|SUCCESS|Requirement based|
|H\_03|Check if search by date is working or not|1)Start date 2) End date 3) Dataframe|Historical stock data within the date range|SUCCESS|Requirement based|
|H\_04|Upon Exiting the program, dataframe should be saved as csv|1)Dataframe 2)File pointer|SUCCESS|SUCCESS|Requirement based|

# Low level test plan

|Test ID|HLT ID|Description|Expected I/P|Expected O/P|Actual O/P|Type of Test|
| :- | :- | :- | :- | :- | :- | :- |
|L\_01|H\_01|Check fi created dataframe has all the necessary columns|1)Dataframe|SUCCESS|SUCCESS|Requirement based|
|L\_02|H\_01\_01|Check if csv properly opened or not|1)File name|SUCCESS|SUCCESS|Requirement based|
|L\_03|H\_02|Check if dataframe doesn’t contain any duplicate data|1)Dataframe|SUCCESS|SUCCESS|Requirement based|

