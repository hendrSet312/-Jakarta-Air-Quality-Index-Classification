# Jakarta Air Quality Index Classification 😷

## Background 
Air pollution in Jakarta is unsafe. According to the IQAir report on August 31 2023, the air pollution index in Jakarta was at 175, with PM2.5 as the primary pollutant ([detik.com](https://news.detik.com/berita/d-6905686/jakarta-peringkat-1-kota-paling-berpolusi-sedunia-versi-iq-air-siang-ini)). This pollution issue has dangerous effects on the citizens of Jakarta. The Health Department in Jakarta have said there were 119,734 reported cases of respiratory diseases in March 2023. Furthermore, according to IQAir, this issue of pollution has resulted in approximately 8,100 deaths around the year 2023 ([CNBC Indonesia](https://www.cnbcindonesia.com/research/20230820230330-128-464477/polusi-udara-jakarta-presiden-batuk-ribuan-warga-bisa-tewas )).

## Project description
This project aims to classify the AQI score index with several machine learning methods, decision tree, KNN classifier, and random forest. To classify the AQI score, we use hourly weather data and air pollution data in jakarta (Coordinate : -6.1818,106.8223) from open-meteo website (open-meteo.com) on date range of 06 August 2020 - 10 October 2023.

## AQI Score 
The label of this classification project is AQI score index. This score is commonly used in US to track and report air quailty. The label suits the characteristic of dataset, where the AQI score in the air pollution data is not hazardous (301 and above).  
AQI index score : 
	- 0-50 (good) (1)
	- 51-100 (moderate) (2)
	- 101-150 (unhealthy for sensitive groups) (3)
	- 151-200 (unhealthy) (4)
	- 201-300 (very unhealthy) (5)

 ## Data Description 
### Air Quality Data :
1. Time : the hour and date of collected data
2. pm10 : particulate matter small than 10 µm (μg/m³)
3. pm2_5 : articulate matter small than 2.5 µm (μg/m³)
4. carbon_monoxide : carbon monoxide quantity on 10 meter above ground (μg/m³)
5. nitrogen_oxide : nitrogen oxide quantity on 10 meter above ground (μg/m³)
6. sulphur_dioxide : sulphur oxide quantity on 10 meter above ground (μg/m³)
7. ozone : ozone quantity on 10 meter above ground (μg/m³)
8. uv_index : the uv index, considering the clearness of sky and clouds
9. us_aqi : AQI
	- 0-50 (good) (1)
	- 51-100 (moderate) (2)
	- 101-150 (unhealthy for sensitive groups) (3)
	- 151-200 (unhealthy) (4)
	- 201-300 (very unhealthy) (5)

### Weather Historical Data :
1. time : the hour and date of collected data
2. temperature_2m : air temperature at 2 meters above ground
3. relativehumidity : relative humidity at 2 meters above ground
4. windspeed_10m :  wind speed at 10 meters above ground
5. winddirection_10m : wind direction at 10 meters above ground
6. is_day : the day condition in the observed location (day = 1 , night = 0)


## Data Preprocessing  
Before we had trained the data, we did a data preprocessing. Data preprocessing is a process to clean and transform data. Data preprocessing is a important process to ensures the used data is usable, unbiased and results great performance of model. The used data preprocessing methods in this projects are : 
1. Outlier removal : to remove outlier on the numeric data
2. Multicollinearity column removal : to remove features with multicollinearity 
3. Feature interaction : to create more features that likely support the model performance
4. Oversampling label : to stabilize the label data distributions 

## Training
After we transformed the data, we used the data for training process. The training process uses many machine learning algorithm such as decision tree classifier , KNN Classifier and random forest classifier. We also compared the performance of every model using accuracy, precision, recall and F1 score. 
