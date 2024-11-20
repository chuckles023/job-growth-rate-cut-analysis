# Labor Market FED Cut Analysis


February 23, 2024

The relationship between job growth, the unemployment rate, and monetary policy decisions is important to understanding the trajectory of the US economy at large.  Employment level, represented by PAYEMS in the FRED database, shows the amount of non-farm workers in the US economy.  Trend employment growth is the monthly job creation needed to maintain a stable unemployment rate at the Federal Reserve’s target rate of around 5%.  Speeches from Federal Reserve officials, including Governor Christopher J. Waller, Governor Adriana D. Kugler, and Chair Jerome Powell, provide insights into current labor market dynamics and the Fed’s approach to achieving its 2% inflation target. 

The FRBSF Economic Letter from October 2016 discusses the importance of determining trend job growth in the U.S. labor market and its relevance to maintaining a healthy economy. Estimates suggest that normal trend growth ranges from 50,000 to 110,000 jobs per month, considering factors such as demographic change and labor force participation trends. The Bureau of Labor Statistics' monthly job reports are a crucial economic indicator, providing a timely snapshot of the labor market.  In 2016 when the article was written, payroll job gains had averaged over 200,000, the article anticipated a slowdown as the labor market approached the Federal Reserve's maximum employment goal.

The concept of trend employment growth is defined as the monthly rate required to hold the unemployment rate constant at the Federal Reserve's maximum employment mandate. Historical trends show that job growth is usually above trend during times of economic growth and below trend during times of economic slowdown. The calculation of trend job growth considers factors such as population growth, labor force participation rates, and the natural rate of unemployment. It traces historical trends from the 1960s to the present, with estimates ranging from 60,000 to 160,000 jobs per month.  

The role of labor force participation, especially among different age groups, is identified as a significant source of variation in trend job growth. The overall participation rate, influenced by demographic changes, impacts the overall trend. Projections based on different scenarios of demographic-specific participation rates range from 57,000 to 106,000 jobs per month, highlighting the impact of factors such as aging populations and changes in participation rates on future job growth. Despite uncertainties,  job growth can slow from recent levels and still be considered at or above trend, indicating a resilient labor market.

On January 16th of this year, Governor Christopher J. Waller discussed the economic outlook based on numbers from late 2023\.  The speaker notes positive trends in real GDP growth, low unemployment (below 4 percent), and core PCE inflation running close to 2 percent for the last six months. The analysis suggests that the economy is on a favorable trajectory, but the sustainability of these trends is uncertain.

Waller believes that there is an overall trend of moderation in labor market conditions despite a December increase in job creation which he believes is noise against the trend.  October 2023 saw an increase in 105,000 jobs, November saw 173,000, and then December with 216,000.  Despite the rising numbers, Waller expects the reports to be revised down.  Ultimately, Waller sees a balancing of the labor market with variables like payroll gains, wage growth, and labor force participation cooling off.  Labor demand will be a very important factor to keep an eye on as it will have a direct effect on unemployment.  If the demand declines, it is possible that employment will grow more than job vacancies will be filled.  In May 2022, Waller and Andrew Figura(FED Economic Researcher) derived the theoretical relationship between job vacancies and the unemployment rate to determine how restrictive monetary policy would affect unemployment.  They found that restrictive monetary policy shrunk vacancy rate with a small increase in the unemployment rate which would help the FED bring down inflation.  

The FED is still targeting a 2 percent rate of inflation, so any rate cuts will depend on how they decide to approach that target.  Core PCE inflation fell from 5% in January to 3.2% in November last year which shows a positive trend.  Due to all the trends described, Waller believes that if we are able to obtain a sustained 2% inflation rate, the FOMC will be able to lower the target range for the federal funds rate.   If/When there are rate cuts, Waller expects them to be slow and small to limit reactionary effects.  

On February 7th, Governor Adriana D. Kugler gave a speech on the recent economic developments in the US and Monetary Policy.  Kugler cites a decrease in core PCE inflation as a major indicator of progress in the cooling of inflation.  The moderation of wage growth is one factor helping the recent trend of disinflation.  Like in Waller’s speech, Kugler cites an overall trend of moderation despite recent hikes.  Looking at the Job Openings and Labor Turnover Survey, the ratio of job openings to unemployment has come down closer to pre-pandemic levels indicating a cooling of labor demand along with an increase in labor supply bringing us closer to levels consistent with the target 2 percent inflation.  Kugler concludes that the federal funds rate is likely at its peak and will be reduced appropriately in line with the target inflation rate, but it might stay steady depending on how disinflation continues.  

Chair of the FED, Jerome Powell, spoke on plans for the near future at the January 31 FOMC press conference.  Like Kugler said, the federal funds rate is likely at its peak and the FED will look at decreasing the rate sometime this year, but they are willing to maintain the current rate depending on how inflation moves in the near future. When asked about when it is likely we will see the first cut, Powell responded that the board will probably not have the confidence to start cuts until after their march meeting.  He repeats that the number of cuts that will happen this year is all based on data coming in the near future and they really want to play it safe with how they implement policy.  However, Powell does state that if they see a weakening in the labor market or persuasively low inflation, they could be driven to cut rates sooner than later.  Powell noted that the median participant on the board wrote that they expect 3 rate cuts this year.  From this press conference, we get a somewhat clearer view of the FED’s intentions moving forward as they monitor both inflation and unemployment levels.


## Method:

To determine how the FED will play with interest rates, we will forecast the growth of employment over the next 12 months using the first difference of total employees(nonfarm).  As we know, normal levels of growth range from about 50,000 to 110,000 new jobs every month, and if there is a sustained amount of above trend job growth, unemployment will be pulled below the natural rate.  The level of growth over trend we will be looking for is the 200,000 mark, that can possibly indicate a point where the FED will decide to intervene.  With the FED’s dual mandate of maximum employment and price stability, they will be watching unemployment closely to help determine whether or not they will cut rates. I will also be controlling for pandemic data since it distorts historic data and would have a noticeable impact on the forecast.  


## Econometric Analysis:

<p align="center">
  <img src="https://github.com/chuckles023/labor-market-fed-cut-analysis/blob/main/images/imageproject2_1.png" width="70%">
</p>

**Interpretation:** The first test demonstrates autoregressive behavior, evident in the gradual decay of autocorrelations over time. The slow decline suggests persistence in the data, where current values are strongly influenced by prior observations, indicative of a high degree of temporal dependence.


```
Box-Jenkins \- Estimation by ML Gauss-Newton 
Convergence in    14 Iterations. 
Final criterion was  0.0000052 \<=  0.0000100 

Dependent Variable PAYEMS 
Monthly Data From 1995:01 To 2019:12 
Usable Observations                       300 
Degrees of Freedom                        294 
Centered R^2                        0.6724300 
R-Bar^2                             0.6668591 
Uncentered R^2                      0.7534654 
Mean of Dependent Variable       118.72000000 
Std Error of Dependent Variable  207.41989210 
Standard Error of Estimate       119.71936507 
Sum of Squared Residuals         4213821.5536 
Log Likelihood                     \-1858.9551 
Durbin-Watson Statistic                2.0011 
Q(36-5)                               47.0418 
Significance Level of Q             0.0324401   

Variable                        Coeff      Std Error      T-Stat      Signif 

------------------------------------------------------------------------------------
1\.  CONSTANT                      127.2729807   61.6278070      2.06519  0.03978164 
2\.  AR{1}                           0.0206967    0.0628132      0.32950  0.74201479 
3\.  AR{2}                           0.8740963    0.0618505     14.13240  0.00000000 
4\.  MA{1}                           0.3606328    0.0838646      4.30018  0.00002325 
5\.  MA{2}                          \-0.4769476    0.0705479     \-6.76062  0.00000000 
6\.  MA{3}                           0.1071429    0.0632092      1.69505  0.09112404  
```

<p align="center">
  <img src = "https://github.com/chuckles023/labor-market-fed-cut-analysis/blob/main/images/imageproject2_2.png" width="45%">
  <img src = "https://github.com/chuckles023/labor-market-fed-cut-analysis/blob/main/images/imageproject2_3.png" width="45%">
</p>

<p align="center">
  <img src = "https://github.com/chuckles023/labor-market-fed-cut-analysis/blob/main/images/imageproject2_4.png" width="70%">
</p>

**Interpretation:** Through analysis of the residuals of our model we can firstly reject our null hypothesis that the autocorrelations of our model jointly \= 0\.  We can also reject the null hypothesis that the residuals are normal.  Our AR and MA roots are all less than 1 so we know that our model is invertible and covariance stationary.


## Forecast Results

**Forecast 1:**
<figure style="text-align: center;">
  <img src="https://github.com/chuckles023/labor-market-fed-cut-analysis/blob/main/images/imageproject2_5.png" width="45%">
  <figcaption>Our first forecast is a one-step ahead forecast, showing how our model is able to predict recent data. We see that most of the data of the last 2 years falls within our 95% confidence interval.</figcaption>
</figure>
<br>
**Forecast 2:**
<figure style="text-align: center;">
  <img src="https://github.com/chuckles023/labor-market-fed-cut-analysis/blob/main/images/imageproject2_6.png" width="45%">
  <figcaption>In our second forecast, we predict the level of employment for the year of 2024. The model predicts that February job growth will be over the 200,000 mark and also shows a predicted sustained trend above the normal range of job growth. Despite this, our error band is still quite large, so we can’t predict with certainty that this will be the case over the next year, especially depending on how the FED reacts to upcoming inflation numbers..</figcaption>
</figure>

<table style="width: 100%; border-collapse: collapse;">
  <tr>
    <td>Forecast prediction for 2024:01 (unit: Thousands of Persons)</td>
    <td style="font-weight: bold; text-align: right;">213.01329</td>
  </tr>
  <tr>
    <td>Probability that actual outcome is equal to or less than 200,000</td>
    <td style="font-weight: bold; text-align: right;">0.06260</td>
  </tr>
  <tr>
    <td>Probability that actual outcome is equal to or more than 200,000</td>
    <td style="font-weight: bold; text-align: right;">0.93740</td>
  </tr>
</table>
<br>

## Conclusion:

After consulting our forecasts and applying context from the FED, we can see that the predicted growth in employment could put enough downward pressure on unemployment to cause the FED to step in and make a rate cut.  The probability that job growth stays at or above 200,000 per month is 93.7%.  This is promising as the current portfolio predicts more rate cuts, but I believe that from analyzing what the FED is saying, they will be very patient with rate cuts this year as they try to curb inflation.  While nonfarm payrolls give us important information on one side of the FED’s monetary policy, we need to pay attention to indicators of inflation as the FED is more focused on that front at the moment. 


## Sources:

1. [**https://www.frbsf.org/research-and-insights/publications/economic-letter/2016/10/trend-job-growth-where-is-normal/**](https://www.frbsf.org/research-and-insights/publications/economic-letter/2016/10/trend-job-growth-where-is-normal/)

2. [**https://www.federalreserve.gov/newsevents/speech/waller20240116a.htm**](https://www.federalreserve.gov/newsevents/speech/waller20240116a.htm)

3. [**https://www.federalreserve.gov/newsevents/speech/kugler20240207a.htm**](https://www.federalreserve.gov/newsevents/speech/kugler20240207a.htm)

4. [**https://www.federalreserve.gov/monetarypolicy/fomcpresconf20240131.htm**](https://www.federalreserve.gov/monetarypolicy/fomcpresconf20240131.htm)

[**Google doc backup: https://docs.google.com/document/d/1IRgwqOf9zSLBf6zeM8mOVmH0j1ULXadTMNqyKLDQBIQ/edit?usp=sharing**](https://docs.google.com/document/d/1IRgwqOf9zSLBf6zeM8mOVmH0j1ULXadTMNqyKLDQBIQ/edit?usp=sharing)

