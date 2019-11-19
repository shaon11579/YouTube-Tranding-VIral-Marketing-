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


 Regression21 <- lm(likes ~ Analytic+Clout+Authentic+Tone+affect+posemo+negemo+anger+sad , data = Nov20)
> summary(Regression21)

Call:
lm(formula = likes ~ Analytic + Clout + Authentic + Tone + affect + 
    posemo + negemo + anger + sad, data = Nov20)

Residuals:
    Min      1Q  Median      3Q     Max 
-782648  -44742    2235   44585 1350301 

Coefficients:
            Estimate Std. Error t value Pr(>|t|)    
(Intercept) 212780.5   119338.3   1.783 0.076182 .  
Analytic      1247.5     1085.5   1.149 0.251900    
Clout        -1666.0      738.3  -2.257 0.025170 *  
Authentic      392.1      879.4   0.446 0.656189    
Tone        -10993.8      712.9 -15.422  < 2e-16 ***
affect      -34229.5    69158.8  -0.495 0.621214    
posemo      273537.7    69432.4   3.940 0.000115 ***
negemo      -63176.9    70097.7  -0.901 0.368586    
anger       -36871.8    14461.0  -2.550 0.011570 *  
sad          21805.4    18427.7   1.183 0.238171    
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 150100 on 190 degrees of freedom
Multiple R-squared:  0.8991,	Adjusted R-squared:  0.8944 
F-statistic: 188.2 on 9 and 190 DF,  p-value: < 2.2e-16

> Regression21.1 <- lm(dislikes ~ Analytic+Clout+Authentic+Tone+affect+posemo+negemo+anger+sad , data = Nov20)
> summary(Regression21.1)

Call:
lm(formula = dislikes ~ Analytic + Clout + Authentic + Tone + 
    affect + posemo + negemo + anger + sad, data = Nov20)

Residuals:
   Min     1Q Median     3Q    Max 
-21669  -6549  -3203   1167 233208 

Coefficients:
             Estimate Std. Error t value Pr(>|t|)
(Intercept)  16403.44   16220.81   1.011    0.313
Analytic        46.01     147.54   0.312    0.755
Clout          -91.18     100.35  -0.909    0.365
Authentic     -102.59     119.53  -0.858    0.392
Tone          -132.09      96.90  -1.363    0.174
affect       10591.99    9400.27   1.127    0.261
posemo      -10275.71    9437.45  -1.089    0.278
negemo       -9983.01    9527.87  -1.048    0.296
anger        -3051.86    1965.58  -1.553    0.122
sad          -1527.13    2504.75  -0.610    0.543

Residual standard error: 20410 on 190 degrees of freedom
Multiple R-squared:  0.04463,	Adjusted R-squared:  -0.0006225 
F-statistic: 0.9862 on 9 and 190 DF,  p-value: 0.4528

> Regression21.2 <- lm( view_count ~ Analytic+Clout+Authentic+Tone+affect+posemo+negemo+anger+sad , data = Nov20)
> summary(Regression21.2)

Call:
lm(formula = view_count ~ Analytic + Clout + Authentic + Tone + 
    affect + posemo + negemo + anger + sad, data = Nov20)

Residuals:
      Min        1Q    Median        3Q       Max 
-41447873  -2622737    479884   3239877 111333367 

Coefficients:
            Estimate Std. Error t value Pr(>|t|)    
(Intercept) 19688199    8785205   2.241   0.0262 *  
Analytic       54783      79909   0.686   0.4938    
Clout        -120624      54348  -2.219   0.0276 *  
Authentic      -1423      64735  -0.022   0.9825    
Tone         -680659      52480 -12.970   <2e-16 ***
affect      -1370176    5091194  -0.269   0.7881    
posemo      12934674    5111333   2.531   0.0122 *  
negemo      -4556826    5160306  -0.883   0.3783    
anger       -2165783    1064559  -2.034   0.0433 *  
sad          1468862    1356575   1.083   0.2803    
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 11050000 on 190 degrees of freedom
Multiple R-squared:  0.7611,	Adjusted R-squared:  0.7498 
F-statistic: 67.25 on 9 and 190 DF,  p-value: < 2.2e-16

> Regression21.3 <- lm(comment_count ~ Analytic+Clout+Authentic+Tone+affect+posemo+negemo+anger+sad , data = Nov20)
> summary(Regression21.3)

Call:
lm(formula = comment_count ~ Analytic + Clout + Authentic + Tone + 
    affect + posemo + negemo + anger + sad, data = Nov20)

Residuals:
   Min     1Q Median     3Q    Max 
-26592 -14852  -8585   1359 208941 

Coefficients:
            Estimate Std. Error t value Pr(>|t|)  
(Intercept) 47185.12   25157.36   1.876   0.0622 .
Analytic      -58.76     228.83  -0.257   0.7976  
Clout        -120.28     155.63  -0.773   0.4406  
Authentic    -117.38     185.38  -0.633   0.5274  
Tone         -289.80     150.28  -1.928   0.0553 .
affect        445.10   14579.17   0.031   0.9757  
posemo        749.35   14636.84   0.051   0.9592  
negemo      -2398.17   14777.08  -0.162   0.8713  
anger       -3899.31    3048.48  -1.279   0.2024  
sad          1307.91    3884.70   0.337   0.7367  
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 31650 on 190 degrees of freedom
Multiple R-squared:  0.04457,	Adjusted R-squared:  -0.0006904 
F-statistic: 0.9847 on 9 and 190 DF,  p-value: 0.454

> 
