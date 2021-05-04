# Weather
get precipitation and temperature data (and anomalies and standardized anomalies) of moving temporal windows from places and dates 




The data set of sample should countain at least : 
 - date at format YYYY-MM-DD
 - longitude
 - latitude
 
It could be better if te data set has also a site id column


You have to declare the length of the moving time windows. The
default values are 0 (only the target days), three days and nine
days. 


```R

source("functions/fun_coord_date_weather.r")

# d the data set of sample in the example case le longitude and latitude column are named longitude_grid_wgs84 and latitude"="latitude_grid_wgs84 respectively. 

dw <- get_sample_weather(dsample = d,time_windows=c(0,15,30), dsample_colnames = c("date"="date", "longitude"="longitude_grid_wgs84", "latitude"="latitude_grid_wgs84"),nc_rep=[weather_data_directory],  var=c("precipitation","mean_temp"),output=TRUE,save=TRUE,fileouput=[file_name_to_save_weather])



```
