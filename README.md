# YouTube-Tranding-VIral-Marketing-


#
# Read data from Desktop 
Nov16 <- read.csv(file.choose(),header=T)
install.packages("lm")
library(lm)
names(Nov16)
# Create Regression Model 

Regression13 <- lm(likes ~ posemo + negemo+ anger+ sad , data = Nov16) 

summary(Regression13)

#Regression Model 2 

Regression14 <- lm(dislikes ~ posemo + negemo+ anger+ sad , data = Nov16) 

                              summary(Regression14)

#Regression Model 3 

Regression15 <- lm( view_count ~ posemo + negemo+ anger+ sad+ affect + Tone+ anx , data = Nov16) 
                              
summary(Regression15)

#Regression Model 4

Regression16 <- lm( comment_count ~ posemo + negemo+ anger+ sad+ affect +Tone+ anx , data = Nov16) 
                              
summary(Regression16)
