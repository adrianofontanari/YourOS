# Appendix — Video Transcripts

## Appendix

This appendix includes the transcript of the YourOS Video. These can be used as an additional reference

### YourOS Configuration Video:

Hi and welcome to the YourOS Configuration Video,
in this guide, we will see how to configure the dashboards included in YourOS.

YourOS allows you to keep track of your financial and well-being analytics, making this information always available.

But, How does it work in practice?

YourOS uses Google Forms as a way to input financial transactions and well-being daily data. the surveys are linked with Google Sheets where the data are stored. Finally, the spreadsheets are linked to custom Google Looker dashboards to visualize the data.
The dashboard is displayed in YourOS Obsidian Vault via an embed of the URL.

As a premise, to make the system work properly you will need to access your Google account from Obsidian. If you have security concerns, I would recommend creating another Google account for the YourOS dashboards. 

In this short video, we will see how to set up the system. It might look a bit technical but it is once in a life process. Make sure to follow the steps as presented to ensure a correct configuration.

To open the YourOS Vault, download the Obsidian app from the official website. Next, open the YourOS Vault making sure to enable the plugin from the pop-up message. We will now see how to configure the dashboards. If you are a Notion user the same steps presented in this video do apply. The only difference will be to add the URLs of the Google Forms and Google Looker Dashboards as an embed into your notion pages instead of in Obsidian.

The first key step is to create the Google surveys. Unfortunately, this part requires a bit of copy and paste as we are going to replicate the surveys included in the configuration handbook. To access Google Forms and create a new survey. 
Copy and paste the list of questions as shown in the handbook. In the video, we now see how to copy a few of them. Make sure to select the correct type of questions and do the same for all the questions.
We will now see as an example how to create the date and heart rate variability questions. As per the heart rate variability, we have three options: Balanced, Unbalanced, and Low.
configured as presented in the handbook
Remember to rename the form as YourOS Wellbeing. 
After setting up the well-being survey,  we do the same for YourOS Transactions. A proposed list of transaction categories is included in the handbook
At the end of the process, the survey should be as presented in the Handbook.  Click on the Preview Button Icon on the top right to verify the form has been correctly

We now access the links of the three Google Sheets included in the YourOS handbook.
From the top bar menu click, File, Create a Copy, and Click Create a Copy. Rename the sheet as YourOS Financials YourOS Well-being and YourOS Trends - Home respectively. During the process, a few Google App Scripts will be copied. These scripts are essential to guarantee the correct functioning of YourOS.
After copying the spreadsheet  Your O S Financials, make sure to copy also YorOS Well-Being and YorOS Trends - Home.


The third step is to go to the Google Forms well-being form, click on answers, and link it to the Google sheet well-being survey you have just copied. Repeat the same for your transactions survey, this time by linking it to your financial spreadsheet.

The fourth step is to go back to the Google surveys and fill both questionnaires with demo data. 

This is important to ensure the survey has been correctly configured.

For the fifth step, we will now update the fields of the spreadsheets to support the newly created Google forms. To do so, go to the YourOS Well-being Spreadsheet, and rename the new sheet linked with the Google form indicated by a purple icon as Form Responses.

Finally, access the Answers sheet, select all the columns and rows, and from the menu click on edit find and replace, in the find field write *configure*, and in the replace field write Form Responses, with an apostrophe at the beginning and end as shown in the video.
Make sure to thick the option search in the formulas and thank click replace all. 

Repeat this step for the badges sheet. Finally, do the same for the Financials Spreadsheet, and this time by renaming the new sheet as Transactions and replacing the word configure with 'Transactions' in the New Transactions NW sheet. Add the fields  N. of Shares (VWCE) and Unit Cost (VWCE) as Column H and Column I in the Transactions sheet.

Remember to add an apostrophe at the beginning and end as done for the Form Responses. 

Finally, access the YourOS Trends - Home spreadsheet, select all the columns and rows, and from the menu click on edit find and replace, in the find field write configure, and in the replace with the URL of the YourOS well-being spreadsheet. This time an apostrophe is not needed.
Make sure to use the URL of your spreadsheet and not one of the ones shown in the video.

Sixth step: We are almost there, to finalize the Spreadsheet configuration we now need to configure the scripts. As per the other parts, we will do it for both Spreadsheets (the financial and well-being ones).
So go to the well-being sheet spreadsheet, and click on extensions, and app scripts. This script reorders the values based on the date and guarantees the data displayed in the dashboard is sorted by date. Click on the run/execute button and authorize the script from the popup message. 

Next, go to triggers, create a new trigger, choose sort responses, as the function, and in the type of event select when the form is submitted.
Finally, authorize the trigger as done before for the scripts.

For the YourOS Financials Spreadsheet, we will do the same. This time we have two more scripts Get Prices and Prices today. These scripts download the latest price value for the Stock VWCE and add it to the sheet VWCE. Run the scripts individually and authorize them from the popup message.

Then need to go to activators and create three activators. One with the get price function, based on time and we set a time (e.g. at noon). The other two are sort of responses and prices today that are activated when the module is submitted.

So essentially, Google Sheets will download the latest price value for VWCE every day, and copy it when we submit a form. It will then order the transactions by date.

Additional considerations on how to configure your investment securities, such as stock or bonds, are included in the configuration handbook. 

Seventh step: we will now configure the Google Looker dashboards. To do so, go to the lookerstudio.google.com and activate your free account by filling in the required information. 

Once done, click on the Create button, data sources, Google Sheets, and authorize Google Looker to access your Google Sheets.

We will now add the fields from the Google Sheets we created before. Select the YourOS Well-Being sheet answers sheet. From the list of fields make sure that the field type for the YourOS well-being score, core YourOS Dimensions (Health, Mindset, Growth, Relationships, Financials, Identity), and habit adherence is the percentage. In case it does not, click on the type field, and from numbers select percentage. After that click the explore button on the top right.

Now we do the same for the financial data. Go back to Google Looker, click on click on the Create button, data sources, Google Sheets, YourOS Financials and select New Transactions NW. Click on the add a field, add a calculated field, and create ten fields by copying the formulas included in the "Fields to be created in Google Looker" section of the YourOS configuration handbook. In this guide, we will do it for one field as an example. 

Once you created a field click on the save button and after creating the ten fields click on explore. Note some fields require some input from your side, such as a financial independence number or daily discretionary spending value.

Next, we add the remaining Google sheets of the Financial Spreadsheet as data sources, the same way we did for New transactions NW and Answers. This time we do not need to create new fields. Once each sheet has been added, click on the explore button; go back to Google Looker, and add another sheet as a data source (Important: add all the sheets as data sources)

The eighth step is about copying the dashboards. To do so access the link of the dashboards included in the YourOS configuration handbook. Per each dashboard click on the hamburger menu to create a copy.
We will start with the YourOS Financials Dashboard, when copying the dashboard you will be prompted to a menu, and in the new source data select the the source in the order as presented in the video.
Financials - Transactions
Financials - New Transactions NW
Financials - Diversification - Country
Financials - Diversification Sector
Financials - Asset Allocation
Financials - Portfolio Breakdown
Financials - Diversification - Holdings

Repeat the same step for the other dashboards.
For the YourOS Well-being Insights (Home) pick Financials - New Transactions NW and YourOS-Well-Being - Answers in this order.
For the YourOS Financials - Home dashboard pick Financials - New Transactions NW as a data source

For the remaining dashboards, simply pick the YourOS Well-being - Answers and YourOS Well-being Form responses in this order.

At the end of the process, you should have nine dashboards.

Ninth step: we can now copy the link of the dashboard into YourOS. Go to the YourOS Wellbeing - insights (home) - click on embed report and copy the URL included from the windows. Make sure to copy only the URL. Next, go to Obsidian, click on the gear to access the settings, and custom frames, and paste the URL in the YourOS Wellbeing - insights (home) area. 

You need to open the YourOS Vault in Obsdian.md or use Notion to add the dashboards.

Repeat the same for the remaining YourOS dashboards, paying attention that the name in Obsidian matches the name of the Looker Dashboard.

For the YourOS Trends - Home and YourOS Leaderboard we have to do a few steps more as these are Excel embeds.

Go to the YourOS Well-being spreadsheet. Click on file, share, publish on the web, embed, select leaderboard, and click on the publish button. Now copy only the URL from the window and paste it into the custom frames Leaderboard as we did for the other dashboard.

Now access the YourOS Trends - Home and  Click on file, share, publish on the web, embed, select Main, and click on the publish button. Now copy only the URL from the winds and paste it into custom frames YourOS Trends  Home URL area.

Finally, copy the URLs of the Well-Being and Transactions Sureys Google Forms too.

The final step is to log in with the Google account to have the right to see the dashboards from Obsidian. To do so click on the command palette and select Gmail and access your Google account. Afterwards, restart Obsidian! YourOS is finally set up!

You may have noticed that the spreadsheets YourOS Well-being and YourOS Financials already include some demo data. To start adding your information simply cancel the contents of the cells as shown in this video.

Additional information on how to edit the survey (such as removing the heart rate variability or changing the habits), YourOS dashboard functioning as well as advanced configuration options and design customizations are included in the Handbook.

---

### YourOS Essentials

Welcome to YourOS.
In this video, we will have a walkthrough of the key functions of YourOS.
I recommend reading also the handbook as a complementary guide.

YourOS consists of four integrated components:
1) A Personal knowledge management system
2) A Journaling system with periodic reviews (weekly, monthly, quarterly, annual) and a well-being analytics system (dashboards)
3) A task and Project & Goals manager (as YourOS aims to be a practical tool there is no distinction between project and goals)
4) A financial tracker system

We will now start exploring the home page.
First of all, it is important to notice that, it is normal to see a blank space on some pages. These boxes are meant to include the YourOS Dashboards. If blank, it means a URL is missing. Please follow the YourOS Configuration Video to see how to configure them. Once done, YourOS will look like as presented in this video. The metrics in this Dashboard refer to the trend of the past 7 days compared to the previous 30 days.

Next, there is the task manager, listing the tasks due today. By default, tasks are placed on the page this week. To add a New task simply click command + T from Mac or go to the command palette and click new task. YourOS also features a list of recurring tasks that are listed separately in a note called periodic. 

Next, we have projects. YourOS has a practical focus so there is no distinction between projects and goals. When creating a new project you need to specify a few inputs as shown in the video.

These are the project status, the dimension, the priority, the deadline, the year, the quarter, and the project complexity.

Then we have the knowledge base, structured into the six core dimensions of our lives: Health, Mindset, Identity, Financials, Relationships, and Growth. Each dimension can have linked projects, areas of responsibilities, resources, and an archive. People familiar with the concept of the Second Brain will recall the PARA Method. You can add a new area from the command palette menu.

The home page also includes more detailed analytics on your well-being and financial information. To configure the dashboards refer to the YourOS configuration video.

We will now explore the core elements of YourOS listed in the ribbon.

The Journal System comprises daily, weekly, monthly, quarterly, and annual journals. By clicking on the calendar icon with today's date YourOS will create a daily note. The structure of the note is editable by accessing the templates in the dedicated folder. To add a journal entry click Command + E from Mac, or select the command from the command palette, or enter the diary note directly. YourOS features a few sections that are automatically aggregated into the weekly review note. 

To create a weekly review note, click on the week number from the calendar on the right sidebar. 

Afterward, replace1 with this Monday's date and replace2 with the next Monday's date, in the format year dash month dash day. You can also delete the blue box, namely a callout. YourOS features callouts in all the core pages to guide how to use them.

Reviews are automatically generated by gathering the data input in the daily journal and are structured into the six dimensions of YourOS. 

These are Health, Mindset, Growth, Relationships, Financials and Identity.
So reviews have a section per each dimension combined with the dashboards. This helps you to have diary input, well-being, and financial data in one place.

The final section of the weekly review note is an area for planning the next week. Weekly priorities included here can be copied and replaced with the ones of today's note. Before doing so remember to copy the past weeks' priorities to reflect on the achievements.

You can use this time to also map out the tasks for the past week and archive the tasks completed by moving them to the tasks log. You are done, you have now reflected on the past week by reviewing your project, well-being a financial data. You also planned for the next week. You may want to use the calendar included in YourOS to schedule when to do the key tasks, this planning process is crucial to motivate you to commit to completing each activity.

To create a monthly, quarterly, or annual note, simply create a new note, add the template, and move it to this year's folder. Rename the note with the respective week, monthly, or quarter number.

Now let's go back to the daily journal.
You can log your well-being data and financial transactions simply by compiling the two surveys included on the daily journal page. Follow the steps of the configuration video to configure them properly.

After sending a survey click on the Google Looker icon and refresh the data. By default, Google Looker rephrases the data every 15 minutes.

Use the final section of the journal to plan your next day or review past diary entries on the same day over the years.

Now we will explore other core areas of YourOS.
The Today page shows the activities due today. It also includes the weekly priorities shown in the daily journal.

This page shows the active projects in the short-term (next 12 months), mid-term (next 2-4 years), and long-term (>5 years). Completed projects will appear in the [[🏆 Museum]].

As your Health Data Hub, this page shows your well-being and lifestyle analytics dashboards.

The studio space works as a digital office to process notes and find focus.

Financials allow you to monitor your finances and log new transactions. 

The Harbour page is your safe box when you need some relief. Honor your dear ones, listen to the music you love, read affirmations, or see pictures of your favorite places. The ideas on how to use this section are countless.

The YourOS ribbon includes a few commands, such as starting an audio recording, creating a new canvas, opening the command palette, and the quick switcher to change a note, or a random note. The YourOS Handbook is always accessible from the dedicated button.

Finally, YourOS includes a few more commands to help you get your life organized, such as creating a new person note, a meeting note, or adding an item to the wish list note.
