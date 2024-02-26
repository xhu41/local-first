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

#another example