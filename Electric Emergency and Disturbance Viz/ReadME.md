Electric Emergency and Disturbance Report (Jan.2020- Aug.2022) Dashboard Link: 
https://public.tableau.com/views/ElectricDisturbanceUSA12020-82022/Dashboard1?:language=en-US&:display_count=n&:origin=viz_share_link
Dashboard Source: https://www.oe.netl.doe.gov/OE417_annual_summary.aspx

Summary:
How many times have you experienced blackouts last year? What about the year before? The uploaded Compiled_Annual_Summary Excel 
file is a compiled file of 2020-2022 data from the government website above. (Unfortunately, 2022 file only contains data up to August for now, but 
hopefully, it will be updated soon). The type of questions that can be answered from the Dashboard are:

   -Has there been a shift in the disturbance pattern in the US (2020-2022)?
   -Which states experience the most disturbance?
   -What is the average recovery time for my state?
   -What is the most common reason for the power loss?
   -How many customers were affected each year?
   -How much demand loss was there each year? (Demand in electricity describes how much MegaWatts is needed to run the electricity at a given time.)

Method:
I created a new column called the 'Time Took For Restoration (hrs.)' in Excel by subtracting the 'Time of Restoration' from the 'Time Event Began' column 
and I used Pandas and Regex to clean texts (Check out my Cleaning_Electric_Data.ipynb).

Messy Text:
An example of a row would be something like 'New York: Dutchess County, Orange County, Missouri: Clay County, Jackson County; Kansas: Johnson County;'.
I used REGEX and Pandas to separate the state and its counties from other states and their counties. Using these tools, I was able to compile states 
into one, nice column and counties another. The final cleaned data is on the Final_Cleaned_Data_Electric_Disturbance csv file.



