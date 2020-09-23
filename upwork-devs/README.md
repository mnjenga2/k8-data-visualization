# Visualisations

## 1. Github Issue Visualisations
This project is aimed at comming up with useful visuals and insights to the gitbub issues that are generated on different repositores.
#### Files created
- issues.py: a python script that contains the class and methods that drive the visualisations
- issues.ipynb: jupyter notebook with all the visualisations
#### Required
Generate a github token to be inserted into issues.py, line 19 
![token](https://user-images.githubusercontent.com/8102313/93817512-c37d0880-fc61-11ea-98f3-9a9386ab028d.png)

#### Flow Diagram
![Issue_vis](https://user-images.githubusercontent.com/8102313/93816881-cfb49600-fc60-11ea-9723-47b0ad70d378.png)

#### Usage
(i)  Import dependencies e.g from issues import Issues
(ii) List  repositories to be visualised 
- e.g repos = ['mvp-icap-service', 'mvp-icap-cloud', 'mvp-icap-squid-cache-proxy','c-icap']

(iii) Initialise eg
- issues = Issues(repos)  -> To call issues
- df = issues.get_df()    -> creates dataframe
- issues.important()      -> Select important columns

(iv) Plot visualisations e.g
- issues.show_pie('state') -> pie chart showing open/closed issues
- issues.show_bar_chart_by_repo() -> bar graph showing number of issues per repo
- issues.show_bar_chart_by_date() -> bar graph showing number issues per day
- issues.show_bar_chart_by_user() -> bar graph showing number of issues generated by users
- issues.table_project_state() -> table showing number of open/closed issues per repo
- issues.show_state_user() -> bar graph showing open/closed issues per user