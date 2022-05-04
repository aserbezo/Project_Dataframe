# Project_Dataframe
-Zip archive that contains JSON files with some sensor data
Goal is to :
	- join them with the respective sensor information (sensors.csv) and add the description column.
			- conver the measurments in column "state" 
				- to Farenheit if the sensor name contains temp or deg (the current measure is in Celsius) in its name
				- to MB if there is a memory in the name of the sensor (the current measure is in KB)
				- add percentages sign (%) where the sensor name contains humidity
		* write the result dataframe to a partitioned parquet file partition by date (either taken from the file name or the "created" column) and sensor name
