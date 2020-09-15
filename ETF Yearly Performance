# Load the appropriate libraries 
library(dplyr)
library(ggplot2)
library(tidyr)
library(scales)
library(reshape2)
library(readr)

# Load the dataset 
Rdataset <- read.csv("~/Desktop/RChallenge/Rdataset.csv")

# View the dataset
View(Rdataset)

# Load the data and melt the columns to condense the data 
Rdataset$Date <- as.Date(as.character(Rdataset$Date),"%Y-%m-%d")
data <- melt(Rdataset,id.vars="Date",measure.vars=c(2:10))

# Plot the data onto a plot 
ggplot(data, aes(x=Date,y=value))+ geom_line(aes(color=variable,group=variable))

# Plot the data onto a plot with a smooth trend line 
ggplot(data, aes(x=Date,y=value))+ geom_line(aes(color=variable,group=variable)) + geom_smooth() + scale_y_continuous(trans='log10')
