# Week 10 Calculation of Mean, Median, SD, Mode, and Add&Delete a New Column in R

# R has similar formulas to Excel like mean(), median(), mode(), sd() but R cannot direct work on values
# Try mean(2+3), see what you get?
mean(2+5)
# You must work on a vector or a column of values!
# 1. Mean
# Find the mean for 2 and 5.
# Assign the values to vector x
x<-c(2,5) 
mean(x) 
# If you want to give a name to the result of mean, then name it like
x_mn=mean(x)  # Don't use command names like mean, mode, median as the name

# If we want to drop the 3 numbers in both ends, and want to know the trimmed mean. 
# Apply the trim() as below:
y<-c(1,2,3,4,5,6,7,8,9,10)
mean(y, trim = 0.3)

# If we have NAs in the vector, such as 
x1 <- c(12,7,3,4.2,18,NA,54,-21,8,-5,NA)
# we want to have the mean by excluding NAs:
mean(x1, na.rm = TRUE)  # na.rm(): whether or not to remove NA

# Find the mean for the temperature column using the cityweather.csv
# read the data into R
getwd()
library(readr)
df1 <- read_csv("/Users/xiaoyanhu/Downloads/AP PPOL105 Spring 2023/week10/cityweather.csv") 
# Now we work on df1, which is a duplicate of cityweather.csv
# Names of columns
names(df1)   
# [1] "city_ID" "weekday" "temperature"  
# Find the mean of the column temperature for the entire dataset
mean(df1$temperature)  
# [1] 90.35714
# Can you find the mean for column of city_ID and weekday?
mean(df1$city_ID)
mean(df1$weekday)
