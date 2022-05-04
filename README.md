# US_back_from_Holidays_Air_Traffic

This repo contains the project conducted for the course [Advanced Business Analytics](https://kurser.dtu.dk/course/2021-2022/42578?menulanguage=en). The repo contains the submitted notebooks datasets used. The highlights of the projects are the use of advanced visualizations, statistical tests, using APIs and JSON, and modelling with an explainable AI perspective in mind, using XGBoost with SHAP. 


## Overview

In the so-called technological era that we live in, transport and mobility play a pivotal role in every business planner’s agenda. Travel time losses are only expected to grow as societies grow and new means of transport arise, disrupting the mobility patterns. This travel time losses come at the expense of misinformation, improper planning and ever so more common extreme weather conditions. This project aims to enlighten businesses across the U.S. on key considerations one should take when planning business trips or scheduling events. Furthermore, the report’s findings might also be of utmost interest to airplane carriers and airports, which will find key drivers of customer unsatisfaction.

## Problem
The problem is set by formulating and then investigating research questions as well as defining a prediction engine to determine flights cancelled or delayed in future months of January. The following research questions were examined:

-	Are there any airlines that are most likely to have their flights delayed or cancelled?
-	Are there any routes that are more prone to have flights delayed or cancelled?
-	Does flying on a specific day of the week mean that flights are more likely to be delayed or cancelled?
-	Do the weather conditions have an impact on the airline's activities? If so, which weather conditions are relevant?
-	Which airports are more likely to have cancellations?
-	Can I predict if my flight will be cancelled?
-	Can I predict if my flight will arrive late?

## Summary and Business Insights
Looking into the research questions, specific routes, on which passengers are more likely to experience a flight delay or a cancellation were investigated. It was found out that overall, there is no observable pattern in routes that would repeat in both January 2019 and 2020, however the maps give a straightforward recommendation on which routes to avoid.

Furthermore, no visible relation between flight disruptions and different airline companies was discovered when comparing the two months. However, it was shown that on certain days, a lot of airlines experienced an increase in flight disruption numbers. This can be seen in the picture below:

![image](https://user-images.githubusercontent.com/72278168/166742808-ef747d5d-a505-4f6f-a08c-ac9ea8b09bfa.png)

Looking into days of the week, it was concluded that there was little connection between weekdays and flights disruptions, however local increases in numbers were observed. After investigating these local peaks, it was found out that they were related to isolated events, such as the US government shutdown, or some instances of strong local snowstorms and adverse weather conditions. This naturally led to investigating weather conditions and their impact on flight disruptions. We found that weather has a significant impact on both delays and cancellations. Attributes such as temperature, snow and precipitation specifically play a big role in the likelihood of a flight being cancelled.  Finally, it is concluded that the airports themselves cannot be seen as a cause for cancellations and that unpredictable extreme events such as snowstorms, strikes, etc., can have a huge impact in the correct functioning of airport operations. This is emphasized in the SHAP values of the xgboost prediction, as can be seen below:

![image](https://user-images.githubusercontent.com/72278168/166743363-30e75f59-ff2a-4c83-a1be-86e46ab8bd78.png)

_Note that the values are normalized, hence the small scale._


The last two research questions on predictions were investigated by modelling cancellations and delays using a wide range of predictive models. However, the models were not able to capture causality as they only worked properly making predictions for the year they were trained on, 2019, and they did not perform well when making future predictions and for 2020. This was most likely due to the weather anomalies in the 2019 dataset. Suggestions were made for future work in terms of removing anomalies, gathering more data, and not splitting the datasets in 2019 and 2020.

## Recommendations
Based on the insights obtained, the delays and cancellations of flights are of unpredictable nature, as shown in the analyses conducted. When planning on taking a flight, one should mainly take into account whether there are any extreme weather conditions expected in the weather forecast for both the airport of departure and the final destination, more specifically for the flights departing or arriving to airports located in the Midwest and East part of the United States.
