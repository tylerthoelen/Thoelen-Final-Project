# Thoelen-Final-Project
Using one Qualitative and Quantitative variable, do states with higher average temperatures in August experience lower amounts of annual snowfall?
# thoelet1-final_project.R
#STA 145 Final Project, Activity 3.1: Upload your Data into R

# Step 3: load the tidyverse
library(readr)

# Step 4: set the working directory and load the data

data<-read_delim("STA 145 Climate Stats - Data Table Tabular.csv")

#Step 5: run the three checks
dim(data)
names(data)
summary(data)

# calculate standard deviation

sd(data$snowfall,na.rm=TRUE)

sd(data$snowfall,na.rm=TRUE)

# linear regression
linear_model <- lm(avg_temp ~ snowfall, data = data)
summary(linear_model)
