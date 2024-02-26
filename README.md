## Car Price Prediction
- Overview: A Chinese automobile company Geely Auto aspires to enter the US market by setting up their manufacturing unit there and producing cars locally to give competition to their US and European counterparts. They have contracted an automobile consulting company to understand the factors on which the pricing of cars depends. Specifically, **they want to understand the factors affecting the pricing of cars** in the American market, since those may be very different from the Chinese market.


### Column Dictionary:
- Car_ID: Unique id of each observation (Interger)		
- Symboling: Its assigned insurance risk rating, A value of +3 indicates that the auto is risky, -3 that it is probably pretty safe.(Categorical) 		
- carCompany: Name of car company (Categorical)		
- fueltype: Car fuel type i.e gas or diesel (Categorical)		
- aspiration: Aspiration used in a car (Categorical)		
- doornumber: Number of doors in a car (Categorical)		
- carbody: body of car (Categorical)		
- drivewheel: type of drive wheel (Categorical)		
- enginelocation: Location of car engine (Categorical)		
- wheelbase: Weelbase of car (Numeric)		
- carlength: Length of car (Numeric)		
- carwidth: Width of car (Numeric)		
- carheight: height of car (Numeric)		
- curbweight: The weight of a car without occupants or baggage. (Numeric)
- enginetype: Type of engine. (Categorical)		
- cylindernumber: cylinder placed in the car (Categorical)		
- enginesize: Size of car (Numeric)		
- fuelsystem: Fuel system of car (Categorical)		
- boreratio: Boreratio of car (Numeric)		
- stroke: Stroke or volume inside the engine (Numeric)		
- compressionratio: compression ratio of car (Numeric)		
- horsepower: Horsepower (Numeric)		
- peakrpm: car peak rpm (Numeric)		
- citympg: Mileage in city (Numeric)		
- highwaympg: Mileage on highway (Numeric)		
- price(Dependent variable): Price of car (Numeric)		


#### Training:
- Constructed a Pipeline of a Transformer to encode the categorical features and scale the numerical features and **LinearRegression** model and got an RMSE of 3867.6 and R^2 of 0.81.
- Trained **Ridge** with GridSearch and got RMSE of 3863.9 and R^2 of 0.81
- Trained **RandomForrestRegressor** with GridSearch and got RMSE of 2552.4 and R^2 of .91
- Costructed a custom Transformer for the categorical features and trained it with RandomForrest but didnt perform well.
- Trained **SVC** but performed poorly on the data