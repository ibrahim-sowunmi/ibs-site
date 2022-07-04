---
title: "Salesforce Forecasting Explained"
date: 2022-07-03T11:10:36+08:00
draft: false
language: en
description: I wanted to take some time to go over standard salesforce forecasting in some depth. Going over different aspects of forecasting alongside benefits and people who need it. This written especially for salesforce SEs so someme information may be omitted.

---

I wanted to take some time to go over standard salesforce forecasting in some depth. Going over different aspects of forecasting alongside benefits and people who need it.

Forecasts are arguable the most intimidating feature to a newbie about sales cloud. Personally, I've found it's because it throws a bunch of new terminology at you whilst expecting you to understand how it works. I'll be breaking terms down as they come up.

**What is salesforce forecasting?** 

Forecasting is an art. A science. A means of allowing companies to predict and plan their sales cycles from pipeline, to closed sales and use that information to manage expectation throughout the organisation. Providing the company with a top-down & future facing view of themselves.

* Breakdown - Pipeline
  * Are the stages a customer goes through once they have shown interested and are looking to buy

If dashboards shows the presesent and past, forecasts show the present and future.

**Why are Salesforce forecasts called Collaborative Forecasts?**

Sales Leaders synthesize input from a variety of sales roles, business units, and regions. Frontline sales teams can be of great value here, providing a perspective on the market you hadn’t considered before. 

![image-20220704114756562](/Users/isowunmi/Library/Application Support/typora-user-images/image-20220704114756562.png)

**What can you do with forecasts?**

- Real time access
- Pipeline by category, time frame & sales team
- Forecast amount to review specific opportunities
- edit forecasts in realtime and add reference notes
- Reachout to reps and managers can see changes
- Change category names
- Breadcrumb trail of reports (Who reports to who, reports to who)
- opportunity amounts as the source of truth

Forecasts are composed of opportunities at different stages. These stages also exist within forecast categories. For instance an 8 step opportunity path can be condesed into 5 forecast categories .

**Why do we use forecast categories?**

* **When sales people must commit**
  * Once opportunities end up in the commit category, it's a signal for sales people to go full steam ahead
* **Seperating process from intent**
  * Opportunity stages reflect where a buyer is in the sales process but it doesn't say much about their intent (how likely they are to buy).
* **Communicating upward**
  * Allows the sales team to pick up sentiment from around the entire sales organisation
  * For instance if you have different opportunity stages for different types of deals (new sales vs renewals), this is an excellent way to summarise sales
* **Summarise opportunity stages**
  * If an opportunity has a variety of stages, forecasting can summarise this as seen in the image below (8 opportunity stages, summarised into 5 forecast stages).

![image-20220704100747876](/Users/isowunmi/Library/Application Support/typora-user-images/image-20220704100747876.png)

**Forecast category stages meaning?**

* **Omitted** -> Opportunities are set to omitted when they are lost or qualified out. For reporting purposes somethings are omitted from the forecasts (eg; renewals). The sales forecasts excludes omitted opportunities.
* **Pipeline** -> A small proportion of the deals in this category will close. Pipeline means a deal is in the pipeline.
* **Best Case** -> Means theres work to be done on these opportunities. Opportunity has a close plan that's coming together (This is what will happen if everything that we expect to close, closes).
* **Commit** -> The close plan is going well on these opps. You have a very very high expectation that these will close ( > 90%). You can confidently rely on these in your forecast. 
* **Closed** -> These are won opportunities. Money in the businesses back pocket. 

![image-20220704114844314](/Users/isowunmi/Library/Application Support/typora-user-images/image-20220704114844314.png)

**Singular vs Cumulative Forecasts**

Forecasts can exist for either a single opportunity record or rolled up into multiple records (to get an overview of a product, business unit, sales team; etc) and that affects what an end-user sees.

* **Omitted (Single)** -> No confidence in winning the opportunity
* **Omitted (Roll-up)** -> N/A

* **Pipeline (Single) ->** An open and working deal with little confidence of winning and close date in the distance
* **Pipeline (Roll-up**) -> All open deals (May exclude early stage opps)

* **Best Case (Single)** -> An open and working deal, usually later in the sales process with high confidence in winning by the expected closed date
* **Best Case (Roll-up)** -> A number you hit if you win EVERYTHING, the best case

* **Commit(Single)** -> An open and working deal in the late stages of the sales process; 99% confident opporuntity will close. 
* **Commit(Roll-up)** -> A comfortable number supported by opportunities. Not worse case. Not a number you miss.

* **Closed(Single)** -> Closed won opportunity.
* **Closed(Roll-up)** -> Sum sales volume of orders booked/contracts signed

![image-20220704163311835](/Users/isowunmi/Library/Application Support/typora-user-images/image-20220704163311835.png)

So think of your forecasts as a probability spectrum. Your job is to figure out wher e your company is most likely to land. Use that information to inform future decisions.

![image-20220704163624189](/Users/isowunmi/Library/Application Support/typora-user-images/image-20220704163624189.png)

So what are some of the benefits of forecasting

**Benefits of forecast?**

- **Zero ambiguity on reps**
  - Can easily drill down and see what reps are/aren't performing via what they have in their pipelines
  - Ability to focus a sales team on high-revenue, high-profit sales pipeline opportunities, resulting in improved win rates 
- **Confidence**
  - Reduction of sales pipeline and forecast risks. Spot challenges before they arise. Maybe you're reps are focusing too much on the pipeline and not enough on the commit stages.
  - Benchmarks that can be used to assess trends in the future
- **Motivation/competition**
  - Encourage friendly competiton between reps/teams by allowing them to view each others pipelines

That's the meat and bone of forecasting. Now for some extras.

**Pipeline Coverage?**

<img src="/Users/isowunmi/Library/Application Support/typora-user-images/image-20220704164321849.png" alt="image-20220704164321849" style="zoom:50%;" />

Measures how close you are to your sales goal. If you set a sales goal of $1 million, and you have $500,000 in your pipeline. Then you have a pipeline coverage ratio of  0.5

*Pipeline coverage ratio = Total pipeline size / Sales Target*

As a rule of thumb coverage should be between 3 - 5. This is valuable but it's the equivalent of asking if it's going to be rainy during your summer trip to Marbella on december. 

So we instead can use weighted pipeline coverage. 

**Weighted pipeline is EE edition only** (This is Expected Revenue)

*Probability of Closing x Deal Value = Weighted Value*

For example, if the opportunity amount is $30,000, and the probability is 30%, then the weighted value is $9,000. This helps paint a more accurate picture of the forecast.

**Salesforce Quota and Gap to Quota?**

* **Quota** -> Is the amount a sales rep need to close for the On Target Earnings (OTE)
* **Gap To Quota** -> The Gap To Quota column lets your sales team know at a glance how close they’re to achieving their quota, without them calculating the gap manually.

**Forecast Types?**

<img src="/Users/isowunmi/Library/Application Support/typora-user-images/image-20220704165229335.png" alt="image-20220704165229335" style="zoom:33%;" />

WTForecast is forecast types. Forecast types source specific pieces of data in different configuration to display sales forecasting pipeline in different lights. These can be custom made, some of the OOTB ones are mentioned below.

**Opportunity Revenue **

Revenue broken down by rep under a given manager

**Product Family Revenue**

Some companies group products and services into families (a group of related goods, for example Oreo (Original Oreo, Oreo white, Oreo mint, Oreo vanilla)).

**Opportunity Splits**

Revenue splitting is sharing the revenue between an opportunity’s team members and to credit the team members who are directly involved a proportional amount. A more granual version on an opportunity split.

**Forecast notes?**

Say you want to change a forecast. You can conveniently make a 



Summary



Sources:



https://help.salesforce.com/s/articleView?language=en_US&type=5&id=sf.forecasts3_forecast_types_overview.htm

https://www.investopedia.com/terms/p/product-family.asp#:~:text=A%20product%20family%20is%20a,customers%20toward%20its%20original%20brand.

https://www.youtube.com/watch?v=sdLe3LBN30A&list=PLFNbZmUNjID4wn4nDVMuwkEwYOT5TaK_1&index=2

https://help.salesforce.com/s/articleView?id=sf.forecasts3_forecast_types_overview.htm&language=en_US&r=https%3A%2F%2Fwww.google.com%2F&type=5

https://www.anaplan.com/blog/sales-forecasting-guide/