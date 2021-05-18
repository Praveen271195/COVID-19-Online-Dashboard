<h1 align="center">Covid-19 Global Dashboard 🦠 </h1>

## Motivation:
This Covid-19 dashboard was created from scratch to visuvalize the global trend of infections and to keep track of the spread of the virus during the pandemic. This dashboard was of a great support to spread awarness amoung the residents of my gated community.

## About the Application:
A web dashboard deployed on Heroku at https://dd-covid-dashboard.herokuapp.com/. Built in Python and Dash, with charts made in Plotly. The data is provided by Johns Hopkins Center for Systems Science and Engineering which is updated every day.


## Resources for Covid dashboard:
- <a href="https://github.com/CSSEGISandData/COVID-19">Covid-19 datasets source</a>
- <a href="https://plotly.com/python/indicator/">Indicator</a>
- <a href="https://plotly.com/python/pie-charts/">Pie chart</a>
- <a href="https://plotly.com/python/line-charts/">Line Chart</a>
- <a href="https://plotly.com/python/bar-charts/">Bar Chart</a>
- <a href="https://plotly.com/python/scattermapbox/">Scatter mapbox</a>
- <a href="https://account.mapbox.com/auth/signin/">Mapbox Account</a>
- <a href="https://dash.plotly.com/dash-core-components/rangeslider">Range Slider</a>
- <a href="https://plotly.com/python/marker-style/">Marker Style</a>
- <a href="https://dash.plotly.com/datatable">Data Table</a>
- <a href="https://plotly.com/python/bubble-charts/">Bubble Chart</a>

## Libraries used:
- <a href="https://pandas.pydata.org/">Pandas</a>
- <a href="https://dash.plotly.com/dash-html-components">Dash HTML components</a>
- <a href="https://dash.plotly.com/dash-core-components">Dash core components</a>
- <a href="https://plotly.com/dash/">Dash</a>

## Description:
Transforming from wide to long format can be done quite simple with Pandas function "melt".


Transforming data from wide format to long format
For more convenient analysis, the next step is to combine confirmed, deaths and recoveries tables into a single one.
The CSSE Covid-19 dataset consists of three tables about daily confirmed, deaths and recoveries cases per country/region. Each table presents the data in wide (crosstab) format, with each day in a column. This format is very difficult to work with. so the first major preprocessing step is to pivot the data in these columns into rows. Transforming from wide to long format can be done quite simple with Pandas function "melt".

Combining Tables


## Instructions to deploy Covid-19 Dash app on Heroku:

1. Sign up for account on Heroku
2. Create your App name (this will be part of the url)
3. Download and install Heroku CLI (allow you to create and manage your Heroku apps directly from the terminal)
4. Create new project in Pycharm (where your app code and files will be located)
a. Choose new environment using Virtualenv
b. Select a python Base interpreter (no need to check the boxes under interpreter)
5. Create a new .py file to start writing the code for your app. If you already created the code for your app, copy those files into your new project folder.
6. Inside your app’s file, under “app = dash.Dash(__name__)”, add this line: server = app.server
7. Open terminal, and cd into your project folder if necessary
8. Pip install any libraries and specific versions your app needs.
    a. pip install numpy
    b. pip install pandas
    c. pip install plotly
    d. pip install dash
    e. pip install gunicorn (needed to run app on heroku)
9. Create .gitignore file inside your project folder (tells Git which files or folders to ignore in a project) and add these lines into it:
    a. venv *.pyc .env .DS_Store (4 separate lines)
10. Create a Procfile inside same folder and add this line inside:
    a. web: gunicorn YourAppFileWithout.py:server
11. Create requirements. Go back to terminal, cd to project folder if necessary, and type:
    a. pip freeze &gt; requirements.txt
12. Inside terminal, type the following- heroku login
13. Then type- git init (don’t forget to ensure you have git installed)
14. heroku git:remote -a AppNameFromStep2
15. git add .
16. git commit -am &quot;initial launch&quot;
17. git push heroku master

## Link to Dash app:

https://dd-covid-dashboard.herokuapp.com/

## Credits:
- <a href="https://www.youtube.com/">YouTube</a> for tutorials
- <a href="https://github.com/CSSEGISandData/COVID-19">JHU CSSE COVID-19 Data</a> for data source
