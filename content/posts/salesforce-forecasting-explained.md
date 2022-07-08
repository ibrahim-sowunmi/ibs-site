---
title: "Salesforce Forecasting Explained"
date: 2022-07-03T11:10:36+08:00
draft: false
language: en
description: I wanted to take some time to go over standard Salesforce forecasting at a high level. This written especially for new Salesforce SEs so some information may be omitted, or may not make the most sense.

---

I wanted to take some time to go over standard salesforce forecasting at a high level.

Forecasts are arguable the most intimidating feature to a newbie in sales cloud as the concept is very foreign. Personally, I've found it's because it throws a bunch of new terminology at you whilst expecting you to understand how it works. Unless you are a sales executive or a quota'd rep, you have likely never come across it before. I'll be breaking terms down as they come up.
 

------

**What is salesforce forecasting?**

Forecasting is an art. A science. A means of allowing companies to predict and plan their sales cycles from pipeline, to closed sales and use that information to manage expectations throughout the organisation. Providing the company with a top-down & future-facing view of themselves.
 

- *Breakdown - Pipeline*
  - *These are the stages a customer goes through once they have shown interest and are looking to buy.*

If dashboards show the present and past, forecasts show the present and future.

------

**Why are Salesforce forecasts called Collaborative Forecasts?**

Sales Leaders synthesise input from a variety of sales roles, business units, and regions. Frontline sales teams can be of great value here, providing a perspective on the market you hadn’t considered before.

------

**What can you do with forecasts?**

- Real-time access
- Pipeline by category, time frame & sales team
- Drill down into Forecast amount to review specific opportunities
- edit forecasts in real-time and add reference notes
- Leaders/Managers can observe manual edits to the forecast
- Pipeline inspection
- Change category names
- Breadcrumb trail of reports (Who reports to who, reports to who)
- opportunity amounts as the source of truth


Forecasts are composed of opportunities at different stages. These stages also exist within forecast categories. For instance, an 8-step opportunity path can be condensed into 5 forecast categories *(See Fig 3, below)*. 
 

![image.png](https://solutions-central.s3.amazonaws.com/prod/post/image-7e346aa0-fe3c-11ec-8b9b-b5d4d6c37193.png)


*Fig 1. Standard Forecast*
 

------

**Why do we use forecast categories?**

![image.png](https://solutions-central.s3.amazonaws.com/prod/post/image-7ada1c10-fe3c-11ec-9a38-edc9e6053091.png)

*Fig 2. OOTB (Out of the box) Forecast Categories* 
 

- **When salespeople must commit**
  - Once opportunities end up in the commit category, it's a signal for salespeople to go full steam ahead
- **Separating process from intent**
  - Opportunity stages reflect where a buyer is in the sales process but it doesn't say much about their intent (how likely they are to buy).
- **Communicating upward**
  - Allows the sales team to pick up the sentiment from around the entire sales organisation.
  - For instance, if you have different opportunity stages for different types of deals (new sales vs renewals), this is an excellent way to summarise sales.
- **Summarise opportunity stages**
  - If an opportunity has a variety of stages, forecasting can summarise this as seen in the image below (8 opportunity stages, summarised into 5 forecast stages).

![image.png](https://solutions-central.s3.amazonaws.com/prod/post/image-7c2f24c0-fe3c-11ec-8b9b-b5d4d6c37193.png)

*Fig 3. Forecast Categories mapped to opportunity stages*

------

**Forecast category stages meaning?**

 

- **Omitted** → Opportunities are set to omitted when they are lost or qualified out. For reporting purposes, some things are omitted from the forecasts (eg; renewals). The sales forecasts exclude omitted opportunities.
- **Pipeline** → A small proportion of the deals in this category will close. Pipeline, means an opportunity has a change of closing.
- **Best Case** → Means there's work to be done on these opportunities. The opportunity has a close plan that's coming together (This is what will happen if everything that we expect to close, closes).
- **Commit** → The close plan is going well on these Opportunities. You have a very very high expectation that these will close ( > 90%). You can confidently rely on these in your forecast.
- **Closed** → These are won opportunities. Money in the business's back pocket.


 

![image.png](https://solutions-central.s3.amazonaws.com/prod/post/image-7b33fbe0-fe3c-11ec-9a38-edc9e6053091.png)

*Fig 4. OOTB (Out of the box) Forecast Categories Again!*

------

**Singular vs Cumulative Forecasts**


Forecasts can exist for either a single opportunity record or rolled up into multiple records (to get an overview of a product, business unit, sales team; etc) and that affects what an end-user sees.
 

- **Omitted (Single)** → No confidence in winning the opportunity
- **Omitted (Roll-up)** → N/A
- **Pipeline (Single)** → An open and working deal with little confidence of winning and close date in the distance
- **Pipeline (Roll-up**) → All open deals and not closed won/lost (May exclude early-stage opps)
- **Best Case (Single)** → An open and working deal, usually later in the sales process with high confidence in winning by the expected closed date
- **Best Case (Roll-up)** → A number you hit if you win EVERYTHING, the best case
- **Commit(Single)** → An open and working deal in the late stages of the sales process; 99% confident opportunity will close.
- **Commit(Roll-up)** → A comfortable number supported by opportunities. Essentially the worse case. Not a number you miss.
- **Closed(Single)** → Closed won opportunity.
- **Closed(Roll-up)** → Sum sales volume of orders booked/contracts signed


![image.png](https://solutions-central.s3.amazonaws.com/prod/post/image-7d749d10-fe3c-11ec-8b9b-b5d4d6c37193.png)

*Fig 5. Difference Between Individual and cumulative categories*

So think of your forecasts as a probability spectrum. Your job is to figure out where your company is most likely to land. Use that information to inform future decisions.

![image.png](https://solutions-central.s3.amazonaws.com/prod/post/image-7dd5cfe0-fe3c-11ec-8b9b-b5d4d6c37193.png)

*Fig 6. Best case vs commit, with actual numbers lying between*

 

------


So what are some of the benefits of forecasting.
 

**Benefits of Forecasting?**

- **Zero ambiguity on reps**
  - Can easily drill down and see what reps are/aren't performing via what they have in their pipelines
  - Ability to focus a sales team on high-revenue, high-profit sales pipeline opportunities, resulting in improved win rates
- **Confidence**
  - Reduction of sales pipeline and forecast risks. Spot challenges before they arise. Maybe your reps are focusing too much on the pipeline and not enough on the commit stages.
  - Benchmarks that can be used to assess trends in the future
- **Motivation/competition**
  - Encourage friendly competition between reps/teams by allowing them to view each other's pipelines

That's the meat and bones of forecasting. Now for some extras.

 

------

**Pipeline Coverage?**

![image.png](https://solutions-central.s3.amazonaws.com/prod/post/image-7b746040-fe3c-11ec-9a38-edc9e6053091.png)


 

*Fig 7. Pipeline coverage*

Measures how close you are to your sales goal. If you set a sales goal of $1 million, and you have $500,000 in your pipeline. Then you have a pipeline coverage ratio of 0.5

*Pipeline coverage ratio = Total pipeline size / Sales Target*

As a rule of thumb, coverage should be between 3 - 5. This is valuable but it's the equivalent of asking if it's going to be rainy during your summer trip to Marbella in December.

So we instead can use weighted pipeline coverage. 
**Weighted pipeline is EE edition only** (This is the Expected Revenue feature)

*Probability of Closing x Deal Value = Weighted Value*

For example, if the opportunity amount is $30,000, and the probability is 30%, then the weighted value is $9,000. This helps paint a more accurate picture of the forecast.

**Salesforce Quota and Gap to Quota?**
 

- **Quota** → Is the amount a sales rep needs to close for the On Target Earnings (OTE)
- **Gap To Quota** → The Gap To Quota column lets your sales team know at a glance how close they are to achieving their quota, without them calculating the gap manually.


 

------

**Forecast Types?**


 

![image.png](https://solutions-central.s3.amazonaws.com/prod/post/image-7caabd60-fe3c-11ec-8b9b-b5d4d6c37193.png)


*Fig 8. Pipeline coverage*



WTForecast is forecast type? Forecast types source specific pieces of data in different configurations to display the sales forecasting pipeline in different lights. These can be custom made, some of the OOTB ones are mentioned below.

**Opportunity Revenue**
Revenue broken down by rep (under a given hierarchy) (Exec → Manager → Rep)

**Product Family Revenue**
Some companies group products and services into families (a group of related goods, for example, Oreo (Original Oreo, Oreo white, Oreo mint, Oreo vanilla)).

**Opportunity Splits**
Revenue splitting is sharing the revenue between an opportunity’s team members and to credit the team members who are directly involved. Same as opportunity Revenue but more granular.

**Forecast Adjustment (W Notes)**

![image.png](https://solutions-central.s3.amazonaws.com/prod/post/image-7d35bf50-fe3c-11ec-8b9b-b5d4d6c37193.png)

![image.png](https://solutions-central.s3.amazonaws.com/prod/post/image-7bc0ab80-fe3c-11ec-9a38-edc9e6053091.png)


*Fig 9. Forecast Adjustment with notes*
 

When a sales leader or manger alters the forecast they can easily add a note to explain what’s going on.


General Tip: You can also use the pipeline inspection feature. Search guides in Solution Central!


That’s the basics of forecasting in salesforce. Fin.
 