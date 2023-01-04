<h1 align = "center"> Bellabeat case study </h1>
<img src = "https://media-exp1.licdn.com/dms/image/C4D0BAQEJ_LS2gJfJWA/company-logo_200_200/0/1604095919872?e=2159024400&v=beta&t=snwBfT14oFk-sOKedz7ykzhZ_ijoV8ddhOlFIaMYZBs" align = "right">
<h4 align = "left"> Agnieszka Karolina Szewczyk <br>
4/01/2022 </h4><br><br><br><br>

<h2> INTRODUCTION </h2>
<p> This project was the capstone of the Google Data Analytics Certificate. I have decided to use Excel and R to complete this task. This was my first project using R.</p>
<h3> SCENARIO </h3>
<P>You are a junior data analyst working on the marketing analyst team at Bellabeat, a high-tech manufacturer of health-focused products for women. Bellabeat is a successful small company, but they have the potential to become a larger player in the global smart device market. Urška Sršen, cofounder and Chief Creative Officer of Bellabeat, believes that analyzing smart device fitness data could help unlock new growth opportunities for the company. You have been asked to focus on one of Bellabeat’s products and analyze smart device data to gain insight into how consumers are using their smart devices. The insights you discover will then help guide marketing strategy for the company. You will present your analysis to the Bellabeat executive team along with your high-level recommendations for Bellabeat’s marketing strategy. </P>
<br>
<H2> ASK </H2>
<h4> 1. Business task: </h4>
<p> To analyse Bellabeat's competitor's smart devices usage data in order to identify potential growth opportunities and recommedations for marketing strategy based on the trends found in the analysis. </p>
<h4> 2. Key stakeholders: </h4>
<p> Urška Sršen: Bellabeat’s cofounder and Chief Creative Officer <br>
Sando Mur: Mathematician and Bellabeat’s cofounder; key member of the Bellabeat executive team <br>
Bellabeat marketing analytics team: A team of data analysts responsible for collecting, analyzing, and reporting data that helps guide Bellabeat’s marketing strategy.</p>
<h4> 3. Questions for the analysis:</h4>
<ul>
  <li> What are some trends in smart device usage and how these trends apply to Bellabeat customers? </li>
<li> How could these trends help influence Bellabeat marketing strategy and help gain new customers? </li>
  </ul><br>

<h2> PREPARE </h2>
<ul>
<li> The data comes from FitBit Fitness Tracker Data, stored on Kaggle, and contains total of 18 csv files. Dataset was generated by by respondents to a distributed survey via Amazon Mechanical Turk between 03.12.2016-05.12.2016. Thirty eligible Fitbit users consented to the submission of personal tracker data, including minute-level output for physical activity, heart rate, and sleep monitoring. Individual reports can be parsed by export session ID (column A) or timestamp (column B). Variation between output represents use of different types of Fitbit trackers and individual tracking behaviors / preferences. </li> <br>
  <li>The licence is listed as a public domain.</li> <br>
<li> The data provided has few limitations. The Small sample size (33 participants)and the fact that the device was collecting data for just one month could mean that the data is biased and not accurately represents the whole population. 
I also think that it lacks important data about the users participating such as gender, current lifestyle and age.</li>
</ul>
<h4> ROCCC analysis </h4>
<ul>
<li> Reliability : LOW – dataset was collected from 30 individuals  who have been tracked for just 1 month. There are missing key indicators such as gender, age and lifestyle </li>
<li> Originality : LOW – third party data collected using Amazon Mechanical Turk.</li>
  <li> Comprehensive : MEDIUM – Multiple data frames with different information </li>
<li> Current : MEDIUM – data is 7 years old. People tend to have their own habits which are not likely to change very fast, but it might not be the best reflection on current trends. </li>
  <li> Cited : HIGH – data collector and source is properly documented.</li> </ul><br>
<h2> PROCESS </h2>
<h3> Data selection & Cleaning</h3> <br>
<p>I have downloaded and opened each file in Excel.</p>
<ul>
  <li> For every file the formatting of the date was changed from CUSTOM to Short date to ensure all dates are uniform</li>
  <li>I have also performed a quick check for duplicate rows by utilising the IF(COUNTIFS()) functions.</li>
  <li>The next steps were to obtain count of unique customer values by using  COUNT(UNIQUE())  formulas  and gathering the information on what data is stored in each file by using TEXTJOIN function.</li>
  <li>The information obtained by performing the 2 last steps was transferred to separate spreadsheet.</li>
  </ul><br>
<p>Upon closer look I have identified that the file dailyActivity_merged.csv contains the data from  dailyCalories_merged.csv, dailyIntensities_merged.csv, and dailySteps_merged.csv therefore I won't be using those.<br><br>
I had a look at the heartrate_seconds.csv file and although monitoring heart rate has plenty of benefits  in day to day life as well as during activities , I won't be getting deeper into analysing this data set due to low number of users (only 7). It is worth noting that the popularity of such devices growing and more people are being aware that the monitoring of heart rate could be vital for ensuring  good health. This could be a good feature to include in Bellabeat devices. </p> <br>
<p>After performing basic cleaning and checking of data in Excel, I will now move to R.</p>
<h4>The whole code written in R can be found in a file called "RMARKDOWN" </h4>

