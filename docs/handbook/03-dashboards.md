# YourOS Dashboards

## YourOS Dashboards 

### Introduction 

YourOS Dashboards are an integral component of YourOS and allow you to easily keep track of and monitor your well-being and financials. Kindly note they require a bit of configuration explained in the next section.

As a simplified version of a recent [Harvard Study](https://hbr.org/2023/12/use-strategic-thinking-to-create-the-life-you-want)] on the areas of our lives, YourOS is structured into six core dimensions: Health, Mindset, Identity, Financials, Relationships and Growth. 

The idea with well-being analytics is not to objectively and scientifically define each dimension but to track the trends to identify areas that require more attention, both in terms of dimensions and habit tracking. 

The user will have to fill out a quick well-being survey every day + log each transaction via the form. Transactions can also be added directly in the Google sheet file (e.g. every week). I recommend doing it regularly to have the financial data expenses.

The questionnaire is subjective and takes about 30 seconds to complete, after some practice. It is designed to be a quick tool that provides a snapshot of well-being according to the 80/20 principle.

As it is a customizable approach, the questionnaire can be designed to be completed daily, weekly, or monthly (for those with less interest but still want to have some high-level data). Before applying changes to the question I recommend configuring the system as presented in the next section to get some familiarity.

The idea is that combining quantitative (AWB) and qualitative dimensions allows for a more complete and accurate view.

##### How metrics are computed
YourOS estimates a Well-Being Score (YWB) as a simple average of each dimension. Each dimension (Health, Mindset, Identity, Financials, Relationships, Growth) is equally valued: given a 100 AWB score, each dimension is worth 16.67%.

Each variable within each dimension carries equal weight. For example, if a dimension has 5 questions, each question counts for 20% of the dimension. This is because it is difficult to say, for example, whether mood weighs more or less than sleep quality (it is therefore a simplification).

Health is an exception, with a score consisting of 50% Heart Rate Variability  (HRV) and 50% subjective questions. This HRV is used as a proxy of the general well-being of a person (Reference [Harvard](https://www.health.harvard.edu/blog/heart-rate-variability-new-way-track-well-2017112212789)). If people do not have trackers and would like to measure their HRV I suggest checking out the HRV4training App (https://www.hrv4training.com/)

### Configuration Guide:

The YourOS Configuration Video is an integral part of this section.

The YourOS Dashboards works as follows: a Google Form questionnaire is connected to a Google Sheet, which in turn is connected to Google Looker Studio for data visualization. This allows integration via iframe to Obsidian - YourOS Vault and full long-term control over the data (effectively, it is an Excel file that can be uploaded to any data visualization tool even in a few decades).

The system consists of 14 components:
- Google Form (2): YourOS Well-being Form, YourOS Financial Transactions Form
- Google Sheet (3): YourOS Well-Being, YourOS Financials, YourOS Insights Home
- Google Looker (9): YourOS Well-being Insights (Home), YourOS Well-being, YourOS Financials - Home, YourOS - Trends, YourOS - Habits, YourOS Well-being Longitudinal Insights, YourOS Well-being Insights - days of the week, YourOS - Financials, YourOS Well-being - daily insights
- **App Scripts (included in the dashboards)**

The configuration should take around 30-45 minutes. I understand it may look a bit technical, and I tried to simplify the passages as much as possible, in case anything is not clear feel free to reach out with your question (email: youros.configuration@gmail.com).

**Unauthorized distribution of the links is strictly prohibited**

| Name                                          | Type          | Link                                                                                                         |
| --------------------------------------------- | ------------- | ------------------------------------------------------------------------------------------------------------ |
| YourOS Well-Being                             | Google Sheets | [Link](https://docs.google.com/spreadsheets/d/1_w1mJA1aZA-Ag4--GLhN_wrIQcMsETibFGD24RC-01c/edit?usp=sharing) |
| YourOS Financials                             | Google Sheets | [Link](https://docs.google.com/spreadsheets/d/10H-3MbbaExtXKMmdeqzNWwLKUHSTPoLYfT4E0kdzRvI/edit?usp=sharing) |
| YourOS Insights Home                          | Google Sheets | [Link](https://docs.google.com/spreadsheets/d/123YT8RK0hE9nVY1Z9hf2pIFiIRE9fM5ZT3Fou1SNbdM/edit?usp=sharing) |
| YourOS Well-being Insights (Home)             | Google Looker | [Link](https://lookerstudio.google.com/reporting/58e733f2-46e7-46b0-8f92-d36bd6bee1b7)                       |
| YourOS Well-being                             | Google Looker | [Link](https://lookerstudio.google.com/reporting/f02a582d-6d1b-481c-b74d-aefa74d96e7c)                       |
| YourOS Financials - Home                      | Google Looker | [Link](https://lookerstudio.google.com/reporting/76ea4a6c-1df8-4d0e-a2ba-ff21bd2f3bca)                       |
| YourOS Trends - Home                          | Google Looker | [Link](https://lookerstudio.google.com/reporting/300b8c80-f792-4c90-94ce-262eaf2d2ae0)                       |
| YourOS - Habits                               | Google Looker | [Link](https://lookerstudio.google.com/reporting/6b36e454-9bae-41f8-ab1b-0e27529b777e)                       |
| YourOS Well-being Longitudinal Insights       | Google Looker | [Link](https://lookerstudio.google.com/reporting/85ff5fb8-1b13-4ebb-a272-89780574f74b)                       |
| YourOS Well-being Insights - days of the week | Google Looker | [Link](https://lookerstudio.google.com/reporting/b8c1e159-6d48-4dee-be9c-644bb07ccaf0)                       |
| YourOS - Financials                           | Google Looker | [Link](https://lookerstudio.google.com/reporting/a945665a-b1ae-417e-882e-a7e37e72ed64)                       |
| YourOS Well-being - daily insights            | Google Looker | [Link](https://lookerstudio.google.com/reporting/a7567edf-7b94-4ac5-8cf7-551cfcde3053)                       |

Current Limitations:
- The System does not accept transactions for future dates
- The Value of a stock is downloaded once a day
- Bank Transfers are not reconciled meaning that if the user sends a bank transfer from Account A and Account B he will need to record two transactions. Note: the Transfer Category is computed neither as an expense nor a category.
- YourOS is best suited for individual investors who possess a few securities as the configuration and management of several securities in YourOS may be impractical. In this scenario, people may want alternatively to create an investment account in YourOS and only update the balance at a specific timeframe (e.g. once a week), simply by logging the variation of the account balance. In other words, the investment account would work like a Wallet account (without the automatic download of the market price of the securities).
- in the case of investment securities, to get the updated net worth of the day you need to log at least one transaction

##### Configuration details
This section complements the configuration video by providing additional information on the configuration. For design customisation see the advanced configuration guide.

1) YourOS Well-being Form
This is the 30-second well-being survey to be filled every day. The user will need to create a Google form in the same format as the following. Refer to the file "YourOS Surveys.xlsx" when creating the survey.

![](images/813f2ed262f8f7c1237737cf34eee1b4_MD5.jpeg)
![](images/4268e8c7da04826f7a8f8d6c35bb9473_MD5.jpeg)

- Users may find it interesting to know more about their strengths/weaknesses to evaluate daily in the survey. There are many validated personality tests, e.g. the [DiSC assessment](https://www.discprofile.com/what-is-disc).

2) YourOS Financial Transactions Form
This survey is necessary to log financial transactions. The user will need to create a Google form in the same format as the following. Refer to the file "YourOS Surveys.xlsx" when creating the survey.
![](images/c5fb491e15ebd6c34c49486ad2e4796f_MD5.jpeg)

3) YourOS Well-being insights (Home)
This dashboard is displayed on the Home Page.
The metrics in the YWB General Dashboard refer to the trend of the past 7 days compared to the previous 30 days. 

Each dimension has categories based on the score:
- Max if dimension score >= 90%
- High if the dimension score is between 80 and 90
- Midi if the dimension score is between 60 and 80
- Low if the dimension score is between 50 and 60
- Min if the dimension score is below 50
![](images/9056784891db1ef8ee041c06eb802f36_MD5.jpeg)

4) YourOS Trends - Home (Excel)
This view is displayed below the YourOS YWB Home Dashboard. It shows the high/low metrics as well as new and lost achievements.
![](images/7b53ecebd30ee38bce354364bfaca123_MD5.jpeg)

5) YourOS Wellbeing
This dashboard shows the Average value of well-being dimensions (variable) as well as the habit adherence in the last seven days (fixed)

![](images/e4c1745805476c7cd1e5fe30226a555b_MD5.jpeg)
![](images/c47e7a7496efd98c58fb91562d2b21dc_MD5.jpeg)

6) YourOS Leaderboard (excel)
This view shows the well-being badges. Badges are structured into four levels:
- red (min level): adherence below the required level in the last 3 days
- orange: adherence above the required level in the last 3 days
- purple: adherence above the required level in the last 7 days
- green: adherence above the required level in the last 30 days
- yellow (max level): adherence above the required level in the last 120 days

It is possible to edit the badge name, adherence levels (column Rule), and timeframes in the sheet Badges of the YourOS Well-being spreadsheet.

My recommendation is to review the adherence levels after a few months of using YourOS.
![](images/398cb5f18c10f103aa6343008814981c_MD5.jpeg)


7) YourOS - Trends
The Trends dashboard shows the average score of the dimensions over different timeframes.
![](images/66fcb1a6719f27938a8b8e395421624e_MD5.jpeg)

8) YourOS - Habits
The Habits dashboard shows the average score of the habits over different timeframes
![](images/19124d886767aaef32fdf6615fd6b1c2_MD5.jpeg)

9) YourOS Well-being Longitudinal Insights
This dashboard shows the score of the Well-being dimensions and sub-dimensions by calendar date.

_(Excerpt)_
![](images/d613679bc1585b2b5958184bd5195649_MD5.jpeg)
10) YourOS Well-being Insights - days of the week

This dashboard shows the score of the Well-being dimensions and sub-dimensions by days of the week (average). For instance, it can answer the question: is my mood high or low during the weekends?

_(Excerpt)_
![](images/588a0a7eb13d5163aef9d86d7ca8ee7d_MD5.jpeg)


11) YourOS Well-being - daily insights
This dashboard shows today's well-being scores vs the average of the past seven days (along with the habit adherence in the last week)
![](images/a94f0cc01a264ad59be5206cdb7880be_MD5.jpeg)

12) YourOS Financials - Home
This dashboard shows high-level personal finance metrics, such as expenses, income, savings, and latest transactions.

_(Excerpt)_
![](images/9d5f27bd80c0d4c24a2a18ca96c07d14_MD5.jpeg)


13) YourOS - Financials
This dashboard provides comprehensive personal finance monitoring, over net worth composition and trends as well as investment tracking.

_(Excerpt)_
![](images/27bcb5da07b867addb26fbe8823bee0f_MD5.jpeg)

![](images/39fe76c027634c5827d0f57564da3a23_MD5.jpeg)
![](images/74b1128036c56e9ca54c026a8a8ab88c_MD5.jpeg)
![](images/5705f0757119a40c7e429b14411bc14c_MD5.jpeg)

----

### Configuration Notes (see Configuration video for the full explanation)

- When copying the YourOS Financials Looker Dashboard, add the new data sources in the following order:

![](images/de70e3c6e5a95748e18b29dd4c5a8bee_MD5.jpeg)

Financials - Transactions (Final)
Financials - New Transactions NW
Financials - Diversification - Country
Financials - Diversification Sector
Financials - Asset Allocation
Financials - Portfolio Breakdown
Financials - Diversification - Holdings

##### Fields to be created in Google Looker 

> [!warning]
> The Formulas presented are functioning. However, when copying the formulas into Google Looker, you may need to delete and add the "*" signs as well as remove additional spaces. If errors are prompted, try to rewrite the formulas instead of copying them.

1) Expenses
```Google Looker
SUM(CASE
  WHEN Amount < 0 THEN Amount
  ELSE 0
END)
```

2) Net Worth (cumulated)
```Google Looker
IF(FIRST(N. of Shares (VWCE)) = 0, FIRST(Amount total), FIRST(Amount total) + FIRST(N. of Shares (VWCE)) * FIRST(Current Value (VWCE)))
```

3) FIRE Progress (Financial Independence Number)
"FIRE Number" is a value (e.g. 3000000)
```Google Looker
Net Worth (cumulated)/"FIRE Number"
```

4) Income

```Google Looker
SUM(CASE
  WHEN Amount >= 0 THEN Amount
  ELSE 0
END)
```

5) Portfolio Value 
(value of my investment securities)
```Google Looker
first (N. of Shares (VWCE)) * first (Current Value (VWCE))
```

6) Runaway 
(for how many months do I have money left considering my monthly average spending)
```Google Looker
Net Worth (cumulated)/(Expenses/30)
```

7) Saving Ratio 
(how much money I saved in a period
```Google Looker
(Income+Expenses)/Income
```

8) Gain (%)

```Google Looker
((first(Shares VWCE (Cumulative))*first(Current Value (VWCE)))+first(Amount Invested))/first(Amount Invested)*(-1)
```

9) AVG Monthly Spending 
(yearly average monthly spending)

```Google Looker
SUM(CASE
  WHEN Amount < 0 THEN Amount
  ELSE 0
END)
*(-1)/365*30
```

10) Portofolio Gain
```Google Looker
(first(Shares VWCE (Cumulative))*first(Current Value (VWCE)))+first(Amount Invested)
```
###### Correct Fields Type Configuration (Key Dashboards):
In this section, you can check if the fields in the data sources are correctly configured

- YourOS Well-being - Form Responses
![](images/eff00d4cc8d1be507d2778e1a909fa9b_MD5.jpeg)
![](images/7b112bca97cbf111f1d83e5c7a3ceb7f_MD5.jpeg)

- YourOS Well-being - Answers
![](images/91e1c29894a108f7d3b2a782336319e3_MD5.jpeg)
![](images/e84f8983364e74ebc53fc875b299f893_MD5.jpeg)
![](images/cca852e03d103f3f971a46cdf2d2624e_MD5.jpeg)

- YourOS Financials - Transactions
![](images/d02c5de493a7df913214f43c0e957c25_MD5.jpeg)

- YourOS Financials - New Transactions NW
![](images/ffbf30d8057d69c3037e71602b3abb46_MD5.jpeg)
![](images/81aa27feb3d621a3673c3e2d52806cdd_MD5.jpeg)

---
