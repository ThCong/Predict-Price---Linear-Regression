# Predict-Price---Linear-Regression
# 1. Reason: 
The world is evolving at a rapid pace, and technology is producing an increasing number of smart gadgets that successfully serve people's lives. Mobile phones enable users to exchange information, work on the go, and enjoy themselves at any time and from any location. Mobile phones have truly transformed the world. Live your life in a more positive manner. As a result, numerous businesses are increasingly encroaching on the smart mobile industry, offering the best gadgets to meet consumers' expectations.
A BADO electronics business in Asia is aiming to generate competition by building a production base in India, the world's second biggest and most promising market after China. competing with other Asian and European rivals.
Because this is a completely new business, the company entered the market very late because several large corporations had already joined. To ensure the best possible preparation for new products, the management team charged the product development and research teams with determining the basis for determining the selling price for the company's upcoming phone products, as well as conducting a general study of the Indian mobile phone market. As a result, the team will need to investigate the elements that influence phone pricing. The amount to which such elements impact phone price in the Indian market, as these factors might differ significantly from those in the local market.
# 2. Objective: 
Investigate and assess the influence of factors influencing phone pricing. Creating a phone pricing prediction model using the acquired data set's accessible independent variables. It will be utilized to determine how the price fluctuates in relation to the independent variables. As a result, the corporation may change the design, configuration of the phones, business strategy, and so on to reach particular pricing points. Furthermore, using this model would help management comprehend the price dynamics of a new market.
# 3. Dataset: 
<a href='https://github.com/ThCong/Predict-Price---Linear-Regression/blob/main/mobile_price_data.csv'>mobile_price_data<a/> is a large dataset about different types of phones in the Indian market. This data set describes in detail the information and characteristics of the phones.
The data consists of 20 columns of information:
- Name, phone company
- Price (in Indian currency)
- Color
- Screen size (in cm and inches)
- Operating system (OS name and version)
- Number of cores (single core, quad core, octa core)
- Processor speed (in GHz)
- Front camera (resolution parameters of the front cameras)
- Rear camera (resolution parameters of the following cameras)
- Resolution (resolution of the display in Pixels)
- Internal memory (in GB)
- External memory (unit GB)
- Battery capacity (in mAh)
- Phone thickness (in mm)
- Length, width of the phone (in mm)
- Weight of phone (in grams)
# 4. Results: 
  # 4.1 Visualize data
  4.1.1 Analysis of price variable (dependant variable)
  ![image](https://user-images.githubusercontent.com/91537767/220319414-91ec1b03-2c5c-4ec3-bc09-150ca24ba756.png)
 <p> <i> Histogram and boxplot chart of Price Variable </i> </p>
  ![image](https://user-images.githubusercontent.com/91537767/220319702-9d317638-ccdf-49a3-b7fc-f3b2e45fad4a.png) 
  <p> <i> Information about price variable </i></p>
From the two charts above, the group has the following comments:
- The price range spans from 6000 to 61000, the data points are not evenly distributed.
- Sharp kurtosis.
- The red line represents the median line, the blue line represents the moving average. It can be seen that the median is less than the mean, so the histogram is skewed to the right.
- There is no significant difference between the mean and median of the price distribution. (mean = 16706 and median = 14994). This results in low variance and standard deviation (as can be seen in the table standard deviation = 8783).
- 25% data points below 10000, 50% below 14994, 75% below 19459.
- 68% of the data points will be between 16706 - 8784 to 16706 + 8784 or between 7922 and 25490.
  4.1.2 Analysis of categorical variables
* Brand: 
![image](https://user-images.githubusercontent.com/91537767/220320927-06de76f3-2e2e-4765-9079-b27a81dcc361.png)

The first graph shows the frequency of phone brands in the dataset. It can be seen that the frequency in descending order is Xiaomi, Vivo, OPPO, Realme, Infinix, Samsung, respectively. The Xiaomi brand has a much higher frequency than the rest, the frequency of Vivo, OPPO, Infinix and Realme has a relative frequency and there is no big difference. For Samsung, the number of appearances is much less than the rest.
The next chart shows the range of price data by brand. Realme is the brand with the widest price range, Xiaomi, Vivo, Oppo have the average price range, and Samsung and Infinix have a rather narrow price range. Compared to the previous chart, brands with low frequency have narrow data range corresponding to that brand, similar to brands with high frequency. However, there is a special point in the Realme brand when the frequency is only 4th, but the data range is the widest among brands, meaning that the Realme brand has the most phones with the most different price points, maybe they is developing maximum customer segments at as many price points as possible. As for Samsung, while the data range is narrow, its data is concentrated in the high price points, which is understandable given that the price of Samsung phones goes hand in hand with its famous brand.
  
![image](https://user-images.githubusercontent.com/91537767/220321396-25cac376-116d-4a8c-a1b3-e469433afe96.png)

With the boxplot chart mentioned earlier, it is possible to compare the average prices across brands. However, it is difficult to see the difference between the prices. To overcome that, the team uses a bar chart for a more intuitive view, and also ranks the average price in descending order to see the difference clearly. Through the chart, we can see that the average price by brand is not equal. Specifically, the average price in descending order is OPPO, Samsung, Realme, Vivo, Xiaomi and Infinix, respectively. The average price of OPPO and Samsung is almost the same and the highest, the average price of Infinix is the lowest and somewhat deviated from the rest. Looking at the chart, it can be seen that the average price by brand is somewhat dependent on the popularity of that brand, as Samsung and OPPO are famous brands, their prices are slightly higher than other brands.

* Color:

![image](https://user-images.githubusercontent.com/91537767/220321539-56b0714e-6333-44ef-8fc5-7e7e698f0f8d.png)

Blue and black dominate the list. It is not uncommon for rare colors to be unpopular in the Asian market, such as mint, champagne, and sea at the bottom of the list.

![image](https://user-images.githubusercontent.com/91537767/220325245-f64d03d3-beb5-4c72-9f74-1a6adc32e988.png)

Green, silver, white, red, black are colors with wide data range. Gray, yellow gold, purple, green are the colors with the average data series. The remaining colors have a very narrow data range.

![image](https://user-images.githubusercontent.com/91537767/220325442-38012502-c8f2-4a84-b723-f8cb7764f043.png)

The average price also has a marked difference between the colors. The color with the highest average price is white, the color with the lowest average price is yellow gold. In the color variable, almost no conclusions have been drawn regarding the price variable.

* Sim: 

![image](https://user-images.githubusercontent.com/91537767/220325858-7a6ac232-b09d-464e-894f-992159d38c4f.png)

Dual Sim has a much higher frequency than Single Sim, if not that Dual Sim almost appears in most data lines. Therefore, it is obvious that the data range of Dual Sim is wider than the data range of Single Sim.

![image](https://user-images.githubusercontent.com/91537767/220325931-5799a47b-9649-4326-bcfe-5d6f53819738.png)

The average price of dual sim phones is also higher than the average price of single sim phones. This proves that the more sim cards a phone supports, the higher the price of the phone.

*Core: 

![image](https://user-images.githubusercontent.com/91537767/220326105-e3aed229-4332-4d42-a67f-715f40e1844b.png)

Octa Core has the highest frequency and outperforms Quad Core and Single Core. Single Core appears almost infrequently in the data set. That leads to a narrower data range from Octa Core to Quad Core, and finally to Single Core.

![image](https://user-images.githubusercontent.com/91537767/220326191-e8be88a3-5992-4d55-b7a8-c05deef90dd5.png)

The average price has a position change by Number of Errors when Single Core is in 2nd place instead of Quad Core. It can be seen that increasing the number of cores does not mean the price will increase.

* Operation System Version

![image](https://user-images.githubusercontent.com/91537767/220326371-72cfb91f-7f74-44f8-bd06-4747ae225c56.png)

OS version Pie 9 is the version with the highest frequency, followed by Oreo 8 and 10 with average frequency, the lowest is Kitkat version 4
Regarding the data series, the data series of version 10, Pie 9, Oreo 8 and Lollipop 5 have a wide and roughly equal data range. Nougat 7 has medium data ranges while Kitkat4 and Marshmallow have small data ranges.

![image](https://user-images.githubusercontent.com/91537767/220326800-a35e7264-1d6f-44c4-be9a-7c1428092594.png)

The average price of OS 10 version is the highest and much higher than other operating systems, the operating system with the lowest price is Lollipop 5. Through the chart, it can be seen that the average price increased or decrease regardless of operating system version increase or decrease.

 4.1.3 Visualize numerical data

![image](https://user-images.githubusercontent.com/91537767/220327135-638ee6e6-90aa-41af-a13e-0986211a433a.png)

![image](https://user-images.githubusercontent.com/91537767/220327235-4b085cfd-1fe2-448c-8f71-878639311b4d.png)

In general, the price variable is proportional to most of the digital data variables, most clearly shown with the variables of processing speed, ROM, RAM, front cam and rear cam resolution.

![image](https://user-images.githubusercontent.com/91537767/220327365-e45d45bf-5663-445a-b353-3292702a4a7a.png)

The graph above shows the correlation between the variables. However, it is only necessary to focus on the correlation between the price variable and the independent variables. Only one variable has a negative correlation with the price variable, width. The remaining independent variables all have positive correlation coefficients with the price variable. For an overview and clearer view of the correlation of the price with the independent variables, we can take a look at the column chart below.

# 4.2 Build price prediction model
4.2.1 Data Preprocessing before entering the model
4.2.1.1 Convert categorical variable to numerical

When inputting data into the model, the input data must be formatted numerically. However, in many cases, the data contains many categorical variables and it is imperative to convert it to numeric form because many variables actually influence the predictive model and to avoid omitting important variables. The group's data also has 5 categorical variables that need to be converted: phone name, color, number of cores, supported sim slot, and operating system.

![image](https://user-images.githubusercontent.com/91537767/220328103-1bbbc6f6-e7a5-48af-84ed-91c18e43c41d.png)

Next, the "Colors" column will be converted to numeric data in a bibliographic format with the help of the numpy library with the astype(‘category).cat.codes” function.

In addition, in the dataset there are some categorical data but still have numeric meaning and can be converted to numeric such as the column "Number of cores" or "Operating system", "Slots sim support".
+ The “Number of cores” column changes to 1 core, 2 cores, and 8 cores.
+ The column "Support sim slot" changes to 1 or 2 sims.
+ The column “Operating system” changes to the operating version such as 10, 9, 8.7…
4.2.1.1 Separate train-test data and scale data
The team will split the dataset in a 7:3 ratio with the sklearn library. That is, 70% of the data will be included in the predictive model and 30% of the data will be used for testing after selecting the best model.
Because the group's data set is also inconsistent in terms of measurement units between columns such as column price (Indian currency), display size (inches), battery capacity (mAh unit)... Therefore, it is necessary to scale to a common unit of measure for model building. The group chose a standardization method to scale the data. The data after being scaled is as shown in the table below.

![image](https://user-images.githubusercontent.com/91537767/220354229-ecf76ba7-3a06-4cdc-9b14-c37cbcde1a81.png)

![image](https://user-images.githubusercontent.com/91537767/220354292-f58819bd-2d7b-40d1-91ae-691148fa6909.png)

Through the chart above, we can see the correlation between the dependent variable (price) and the independent variables in descending order. ROM and RAM are the two variables with the highest correlation coefficient. Only 2 variables width and battery capacity are still 2 variables with negative correlation coefficients, the remaining variables all have positive correlation coefficients.
4.2.2 Model building
4.2.2.1 Select variables
The fact that the independent variables have a high correlation coefficient with price does not mean that it will be appropriate when building a model. Therefore, a method for selecting variables for the model is necessary. RFE is the method used by the team.

![image](https://user-images.githubusercontent.com/91537767/220354720-44bc1617-608e-4164-8aee-70c5a659fdd1.png)

4.2.2.2 Build Model


Proceed to build the model based on the 9 variables selected in the previous step. The team intends to build 3 models with 7, 8, 9 variables in turn to see the difference between models and draw assessments.
  
* Model 1: Price = a + b*name + c*size + d*os + e*ROM + f*p_cam + g*f_cam + h*battery_power

![image](https://user-images.githubusercontent.com/91537767/220354972-eb12f39a-d1bd-4e77-a578-2b044db64c88.png)

* Model 2: Giá = a + b*name + c*size + d*os + e*ROM + f*p_cam + g*f_cam + h*battery_power + i*depth

![image](https://user-images.githubusercontent.com/91537767/220355299-8ba08c16-0645-4bd5-9f44-82195a2e04cb.png)

* Model 3: Giá = a + b*name + c*size + d*os + e*ROM + f*p_cam + g*f_cam + h*battery_power + i*depth + j*weight

![image](https://user-images.githubusercontent.com/91537767/220355336-bb353ca5-d019-4868-ad3c-5afa6d952d34.png)

* Models Evaluation:
Adjusted R^2 in descending order: model 3, model 2, model 1 (72.9% > 72.6% > 68.6%). Therefore, model 3 is the most efficient of the three models. However, the p-value of the weight variable is greater than 5% (=0.06) while the model 2 has the p-value of the variables all equal to 0. Therefore, it is necessary to use a different metric to evaluate the two models. This figure is the RMSE.

4.2.2.3 Explain statistical number in the model

![image](https://user-images.githubusercontent.com/91537767/220355635-0fed4af8-27df-4e0b-a6dd-823beb2b7c78.png)
  <i> The most effective model </i> <p> </p>
- The method used to build the multivariable linear regression model that the team used is the method of least squares (OLS).
- The monitored variable is the price variable.
- Adj. R-squared = 0.729 means that the independent variables explain 72.9% of the dependent variable (price).
- F-statistic = 73.47: the ratio of variation between sample mean and intra-sample variation is 73.47
- No.Observation = 243: observed line count is 243 lines.
- Df Residuals = 233: total number of observation lines minus the number of observed variables
- Df Model = 9: number of independent variables observed.
- The coef column shows the regression coefficients of the independent variables. We have the following linear regression equation: 
  <b> Price </b> = -2.353e-17 + 0.1541*name + 0.3533*size - 0.3499*os + 0.5297*ROM + 0.2379*p_cam + 0.1649*f_cam - 0.2211*battery power + 0.3125*depth - 0.1303*weight

  * Conclusion:
- The price variable is proportional to the variable name, size, ROM, front cam, rear cam and thickness.
- The price variable is inversely proportional to the operating system variable and battery capacity.
- The volume variable has no relationship with the price dependent variable. (Because p-value=0.600 > 5%)

* Interpretation of meaning:
- When the brand name increases by 1 unit, the price of the phone increases by 0.1541 times other things being equal.
- When the display size increases by 1 unit, the price of the phone increases by 0.3533 times other things being equal.
- When the OS version increases by 1 unit, the price of the phone decreases by 0.3499 times other things being equal.
- When the internal memory increases by 1 unit, the price of the phone increases by 0.5297 times other things being equal.- 
- When the rear cam resolution is increased by 1 unit, the price of the phone increases by 0.2379 times, other things being equal.
- When the front cam resolution is increased by 1 unit, the price of the phone increases by 0.1649 times, other things being equal.
- When the battery capacity increases by 1 unit, the price of the phone decreases by 0.2211 times, other things being equal.
- When the thickness of the phone increases by 1 unit, the price of the phone increases by 0.3125 times other things being equal.
- The volume variable is not statistically significant, so the relationship between volume and price is unknown.

![image](https://user-images.githubusercontent.com/91537767/220356337-5cf4953c-9c9f-4fdc-9db3-6bdaf702f164.png)

In the multicollinear table, most of the VIF indexes of the variables are greater than 2, meaning there is a sign of multicollinearity, but all are less than 10, so the model is accepted.

4.2.2.4 Evaluate model residuals

![image](https://user-images.githubusercontent.com/91537767/220356529-77a227e4-0e5d-47d6-a7a5-513aaede1866.png)

The residual distribution graph has a fairly even bell shape on both sides, we can see that the residuals of the model set are in the range from -1 to 1, the mean is towards 0 and the error is towards 1, so residuals move towards a normal distribution. From that, it can be judged that the regression model is quite accurate.
The RMSE coefficient of the calculated model is 0.5104601285742959. That is, the standard deviation of the errors occurring is approximately 0.52.

# 4.3 Experiments
After building the model, what needs to be done is to experiment and test the model with the test dataset that has been extracted from the previous large data set.
First, the test dataset will only take the variables according to the selected model and scaled according to the standardization method to the same unit of measure as the train dataset.
![image](https://user-images.githubusercontent.com/91537767/220356903-55caaae6-027d-4fc7-bb5d-81cce11400bd.png)

Next, feed this test dataset into the model to get price prediction data. Using the sklearn library to evaluate the r2_score between the predicted price and the actual price in the test dataset, the result is 0.7305363058480527, which means that almost 73% of the variation of the price variable can be explained by the model in while the remaining 27% of the variables remain unaccounted for.

![image](https://user-images.githubusercontent.com/91537767/220356990-8703dd70-1fb3-4853-8831-12cac22fc10f.png)

The data points are mostly concentrated around the bisector between the horizontal and vertical axes, but there are still many points located quite far away. The distribution is therefore considered to be fairly normal.

# 5. CONCLUSION 
  
After the research process, the team has selected the most optimal price prediction model which is the model with 9 variables. These variables are all selected from the RFE method and no variables are omitted. From the model, the team determined that the factor that affects the phone's price the most is the internal memory (ROM). With a corrected R^2 greater than 50%, it can be assumed that the group's study is significant in predicting future prices. However, the study still has some limitations. The fact that the data set is quite small leads to the statistical results of the model not being as expected as well as signs of multicollinearity in the model. Besides, although the selected model is the most effective model, there is still one variable that is not statistically significant. At the same time, there may be more effective methods that the team discovers and applies to optimize the model.
