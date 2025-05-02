# Cricket-Data-Integration-and-Visualization
My mission is to bring the thrill of international cricket into the world of data. You’ve been handed a treasure trove of detailed JSON files—rich with metadata, match insights, player stats, and ball-by-ball action from hundreds of One Day International (ODI) cricket matches. 

Here I am using these to set up my environment:
Snowflake as the central cloud data warehouse.
Snowsight for data exploration and dashboarding.
VS Code to manage and write SQL scripts.
And of course, the Snowflake Web UI to interact with the platform directly.
# Task-1: Ingestion of Data
Ingest the JSON files containing ODI match data. I loaded these files into Snowflake's internal stage using the intuitive drag-and-drop interface.
These raw tables are my foundation, housing untouched data in its most granular form.
# Task-2: Cleaning and Structuring the Data
To bring the order to chaos I parsed the nested JSON structures into clean, tabular formats.
My essential tables are:
match_detail_clean – with match type, venue, and outcome.
player_clean_tbl – structured player stats and identifiers.
delivery_clean_tbl – ball-by-ball event data, parsed and ready for analysis.
# Task-3: Building the Consumption Layer
As I have my clean data now, I want to prepare it for business users and analysts.
I crafted a star schema, complete with fact and dimension tables:
date_dim – to enable time-based analysis.
referee_dim – details about match officials.
team_dim, venue_dim, and match_fact_tbl – tying everything together.
This model allows users to slice and dice data in every imaginable way: by player, by date, by umpire, or by performance metrics.
# Task-4: Bringing It All to Life with Dashboards
Using Snowsight, I created a sleek dashboards that allow stakeholders to explore:
Win/loss trends over time
Player performance comparisons
Match summaries and referee statistics
Every click on the dashboard tells a story—of players, teams, and thrilling cricket moments.
Here is the preview of my dashboard.
![image](https://github.com/user-attachments/assets/c08fcdad-29a4-4acb-8cd9-1a18df992fd2)
![image](https://github.com/user-attachments/assets/14d8ac49-ee20-4fdc-ab14-94edb4604bfe)
![image](https://github.com/user-attachments/assets/8a2952f3-5e43-4e06-94ee-6c1e610578d2)

https://app.snowflake.com/xiitpxt/uk56792/#/match-analysis-dashboard-dQSSNIZ8l
