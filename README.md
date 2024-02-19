# Citi Biki Analysis with Tableau
## Challenge #18
![image](https://github.com/bathl01/Citi_Bike_Challenge_18/assets/145512041/f74772a6-06d6-4f4b-9524-f70e92e5c11c)
## Background
Congratulations on your new job! As the new lead analyst for the New York Citi BikeLinks to an external site. program, you are now responsible for overseeing the largest 
bike-sharing program in the United States. In your new role, you will be expected to generate regular reports for city officials looking to publicize and improve the city program.

Since 2013, the Citi Bike program has implemented a robust infrastructure for collecting data on the program's utilization. Each month, bike data is collected, organized, and 
made public on the Citi Bike DataLinks to an external site. webpage.

However, while the data has been regularly updated, the team has yet to implement a dashboard or sophisticated reporting process. City officials have questions about the program, 
so your first task on the job is to build a set of data reports to provide the answers.

## Instructions
Your task in this assignment is to aggregate the data found in the Citi Bike Trip History Logs and find two unexpected phenomena.

1. Design 2–5 visualizations for each discovered phenomenon (4–10 total). You may work with a timespan of your choosing. Optionally, you can also merge multiple datasets from different periods.
2. Use your visualizations (not necessarily all of them) to design a dashboard for each phenomenon. The dashboards should be accompanied by an analysis explaining why the phenomenon may be occurring.
3. Create one of the following visualizations for city officials:
    * **Basic**: A static map that plots all bike stations with a visual indication of the most popular locations to start and end a journey, with zip code data overlaid on top.

    * **Advanced**: A dynamic map that shows how each station's popularity changes over time (by month and year). Again, with zip code data overlaid on the map.

    * The map you choose should also be accompanied by a write-up describing any trends that were noticed during your analysis.

4. Create your final presentation:

    * Create a Tableau story that brings together the visualizations, requested maps, and dashboards.

    * Ensure your presentation is professional, logical, and visually appealing.
    
## Data Source
1. The initial stage of the project involved acquiring all the monthly CSV files, covering the period from January 2019 to December 2023, from the [Citi Bike Data](https://citibikenyc.com/system-data) webpage and organizing them in a designated folder named "data". The data used in this analysis specifically pertains to the Jersey City region.
2. Subsequently, I established a Jupyter Notebook file, named "[citibike.ipynb](https://github.com/JeremyTallant/tableau-challenge/blob/main/citibike.ipynb)] to systematically clean and combine all the monthly CSV files into a single CSV file for 5 years an a file for 2023 only, in preparation for importing into Tableau for analysis of 5 year trends and past year usage.
3. The following is a comprehensive overview of the data cleansing process:
   * First import pandas.
   * Read in all csv files for a single year in a pandas dataframe,
      * store in a list,
      * concatenate into a single dataframe
      * create start date field
      * group all rides from with the same satart location/end location adding a count for the day
      * due to file format change in feb 2021 rename the columns to common names across years and select only needed columns for analysis
         * StartDate', 
         * 'start_station_id', 
         * 'start_station_name', 
         * 'start_lat',
         * 'start_lng',	
         * 'end_station_id',	
         * 'end_station_name', 
         * 'rideable_type'
         * 'count'  
   
   * Repeat step for the remaining years.
   * Combine all three dataframes into a single dataframe for 5 year analysis.
   * Then save the dataframe to a csv file.
   **Please note that the large size of the CSV files the 5 year file is zipped in git hub and the 2023 file is not included**
## Dashboards
From the Citi Bike data, a homepage and three corresponding dashboards were created to provide a comprehensive analysis and visualization of the data.
### Homepage
* The homepage serves as an introduction to the project, providing a concise overview of its purpose and contents. It clearly summarizes the key insights and findings of each dashboard, allowing for quick and easy navigation.
<img width="1425" alt="Screenshot 2023-02-13 at 8 21 56 PM" src="https://user-images.githubusercontent.com/112406455/218622889-c2c2e218-99cc-4f3f-989b-e50da7169004.png">
