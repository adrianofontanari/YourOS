# Advanced YourOS Configuration (PRO)

### Advanced YourOS Configuration (for PRO Users)

This Bonus section includes ideas for an advanced YourOS Configuration.

A current limitation of YourOS Financials is that it does not support future transaction dates. In the case of investment securities, to get the updated net worth of the day you need to log at least one transaction.

On Heart Rate Variability and Edit the wellness questionnaires
By default, the YourOS Well-being form includes the measurement of the Heart Rate Variability. If you would not like to measure it, follow these steps:
1) delete the question from the Google form
2) access the Google spreadsheet YourOS well-being, go to the sheet Answers, select the cell AO2, and edit it as shown
3) In case you edited the well-being survey and would also like to change the achievements, go to the Badges sheet of the YourOSO well-being spreadsheet and update the fields accordingly. For example, you may want to change the adherence level required to unlock the achievement (column Rule) or change the name of the name of achievement. We saw how to remove the heart rate variability measure. With the same logic, it is possible to edit the well-being questionnaires by adding or removing new questions. The best way to do so is not by deleting columns with the discarded questions from the Google sheet but by first adding the questions to the Google form. Google Forms will automatically add a column to the YourOS Welll-being Google sheet that can be used as input. When you add new questions remember also to review how each dimension is computed in the Answers sheet, and the badges sheets by updating reference cells of the column Level - Today and Level- yesterday and the name of the new variable in the biggest orders sheet. finally, go to Google Looker data sources and update the fields of the answers sheet.
4) How to add stocks or bonds: Securities can be added manually as a transaction. To do so, access the YourOS Financials Spreadsheet, go to the Transactions sheet, scroll down to the bottom of the page add manually the date, the account, and the category should be investment securities or investment pension fund (these are not computed as expenses). Add to column H the number of shares and in column I the unit cost

How to add more than one Investment Securities. By default, YourOS includes the VWCE ETF. The way YourOS tracks each stock is the following:
- Transactions sheet columns H and I to add the N. of shared and individual Unit cost. This means that we will need to manually add two rows per each security we possess. 
- Next, we need to create a new sheet with the name of the security (e.g. VUAA:LON for the Vanguard S&P 500 ETF)
- The next step is to go to the New Transactions NW sheets  and add four columns: 
	- N. of Shares (VUAA:LON) taken from the transactions sheet
	- Current Value (VUAA:LON) retries the info from the VUAA:LON sheet
	- Unit Cost (VUAA:LON) taken from the transactions sheet
	- Shares VUAA:LON (Cumulative): includes N. of Shares (VUAA:LON) and the date
	- VUAA:LON Amount Invested is the N. of Shares (VUAA:LON) times the Unit Cost (VUAA:LON) 
	- Remember to also update the Amount Invested column to include the new security
- Now go the the Portfolio Breakdown and add the security information
- Afterwards, we need to go to App Script, copy the get price script, and create a new one, this time by changing the name of the destination sheet and thicker (in this case VUAA:LON), we will do the same for the price today script. Remember to change the function get price and price today with a different name
- we will also have to set up the two triggers for the new functions to be downloaded
- the final step is to go to data sources of the YourOS Financials - New Transactions NW sheets  in Google Looker, update the fields edit the formula to also include the new security, the fields to be updated by adding up the new security are Gain, Net Worth (Cumulated), Portfolio Gain and Portfolio Value

YourOS is best suited for individual investors who possess a few securities as the configuration and management of several securities in YourOS may be impractical. In this scenario, people may want alternatively to create an investment account in YourOS and only update the balance at a specific timeframe (e.g. once a week), simply by logging the variation of the account balance. In other words, the investment account would work like a Wallet account (without the automatic download of the market price of the securities).

When you add a new stock you may want to update the Diversification - Holdings and Diversification Sector. This information is available on the official website of each security and can be added manually to YourOS by adding new columns updating the & fields and including ti


#### On Design customisations: 
- YourOS components are designed for the dark mode, changing it might alter how it is displayed. YourOS is using the Minimal theme and additional customizations: 
	- Main colors: -  background: #242424; - secondary color #F5D70B. 
	- The Style.css file of the Custom Frame Plugin has been edited to be consistent with the theme: background-color: #242424;
	- To edit the order of the icons in the ribbon see the custom-menu-order css snippet
	- To change the icons in the ribbon you may need to encode an svg file: https://yoksel.github.io/url-encoder/

#### On Dashboard Customisations
You can change the background of the dashboard in Google Looker: In the menus, select Page > Current page settings, then on the right, select STYLE. By default is set to #242424 as the main background color of YourOS.

In the custom frames plugin the following snippets have been added to fit the main theme:
- Google Forms (YourOS Well-being + YourOS Financial Transactions)
```css
.D8bnZd {
    background-color: #242424 !important;
}
.RVEQke {
    background-color: #F5D70B !important;
}
```
- Dashboards:
```css
.backdrop.ng-star-inserted {
background-color: #242424
}

.mat-mdc-progress-bar {
--mdc-linear-progress-active-indicator-color: #F5D70B !important;
--mdc-linear-progress-track-color: #242424 !important;
}

.mat-progress-spinner circle,
.mat-mdc-progress-spinner circle,
.mat-spinner circle {
stroke: #F5D70B !important;
}
```
- Excel (YourOS Leaderboard and YourOS Trends)
```css
.grid-container {
    overflow: visible;
    background: #242424 !important;
}

body {
    background-color: #242424 !important;
    color: #242424 !important;
    font-weight: 0 !important;
    font-size: 0 !important;
    font-family: Roboto,RobotoDraft,Helvetica,Arial,sans-serif;
    margin: 0 !important;
}

#footer {
    background: #242424 !important;
    border-top: 0px #242424 solid !important;
    border-bottom: 1px #242424 solid !important;
    font-size: 0 !important;
    padding: 0px 0px !important;
}

#top-bar {
    /* border-bottom: 0px solid #242424 !important; */
    padding: 0px 0px 0 !important;
}

#doc-title .name {
    font-size: 0px !important;
}

.docs-gm ::-webkit-scrollbar-thumb {
    border-style: solid !important;
    border-color: #242424 !important;
    border-width: 0px !important;
    background-color: #242424 !important;
    border-radius: 0px !important;
    box-shadow: none !important;
}

#top-bar {
    border-bottom: 0px solid #242424 !important;
    padding: 0px 0px 0 !important;
}
.grid-fixed-table th, .waffle th {
    /* border: 9px solid #242424 !important; */
    border-width: 0 0px 0px 0 !important;
}
```

#### On Plugins (recommendations):
- Copilot chat: to use LLMs (e.g. Chatpgt in Obsidian)
- MapView: To create a Map of your places
- Google Photos: to see your Google Photos in Obsidian. You can add this snippet in the Daily Journal Template to see the photos of a date over the years.
```photos
{
  "filters": {
    "dateFilter": {
      "dates": [{
        "month": <% fileDate.format("M") %>,
        "day": <% fileDate.format("D") %>
      }]
    }
  }
}
```
You can also add this snippet in the home page or Journal Template to the photos in one specific period
```
photos
{
  "filters": {
    "dateFilter": {
      "ranges": [
        {
          "startDate": {
            "day": 1,
            "month": 1,
            "year": 2024
          },
          "endDate": {
            "day": 31,
            "month": 12,
            "year": 2024
          }
        }
      ]
    }
  }
}
```
- Google Calendar: You can use Google Calendar with the Google Calendar plugin. I would suggest adding the snippets below to the Today Page, Journal template, and Home page (and changing the timespan of events displayed e.g. 1,7,30).  

```
gEvent
   type: schedule
   timespan: day
```
```
gEvent
   type: schedule
   timespan: today
```
```
gEvent
   type: schedule
   timespan: 1
   date: tomorrow
```

- Toggl Track: to track your time
- ActivityWatch: to track your time on specific Obsidian pages
- CodeStat::Stats: to track how much you write in obsidian
- Readwise Official: to sync Readwise with Obsidian (required Readwise Premium). Consider adding a custom frame for Readwise Reader and use it directly in Obsidian. I would also suggest mapping out your information flow to create a close loop with Obsidian and reduce the number of tools used. Readwise is a good option as it syncs books highlights, and web pages straight to Obsidian. Academics may also want to check how to link Zotero.

#### Journal
You can add an automated weather entry to the journal by adding:
- in the daily journal template: <% tp.user.getWeather() %>
- in templater add getWeather function and copy this function, remember to change the "Cityname"): 
```
curl wttr.in/Cityname?format=”%l:+%c+%t+feels+like+%f/Sunrise:+%S/Sunset:++%s/Moon:++++%m”
```
#### Widgets and Tools ideas (to be added via Custom Frames):
- Garmin/Polar/Strava: to track your fitness stats (it could be added in the Journal Templates)
- Home Assistant: to monitor your House from Obsidian
- Volt.fm to track your music stats (it could be added in the Journal Templates)
- Life Calendar: https://notionsparkles.com/life-calendar
- Gifypet: https://gifypet.neocities.org/
- Plasma Ball: http://www.slightlyinteresting.com/plasmaglobe/plasma.asp
- Lava Lamp: http://www.slightlyinteresting.com/lavalamp/lava.asp
- Others (e.g. weather/time displayed in the home: https://indify.co/,  https://dayspedia.com/

##### YourOS New Year Setup
Each Year there are a few quick steps to do:

- Periodic notes: create a new journal folder for the reference year (e.g. 2024) and change the year also in the settings
- Daily Journal Template: change the tag to the reference year
- Journal Templates: Change the word of the year in the template
- QuickAdd: change the reference year folder for the Journal Entry and Quick Note 
- Create a New Tasks Log Note and Update the link in the Task Manager
- Financials (on Google Looker): update/review the field AVG Monthly spending in runaway
