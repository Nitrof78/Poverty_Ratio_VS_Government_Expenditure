# Poverty_Ratio_VS_Government_Expenditure
Through this project we aim at studying the link between several major government expenditures and poverty level in a country. 
To do so, we'll gather the following World Development Indicators coming from the World Bank Databank Website :
- Current health expenditure (% of GDP)    
- Domestic general government health expenditure (% of GDP)  
- Government expenditure on education, total (% of GDP)    
- Military expenditure (% of GDP)   
- Research and development expenditure (% of GDP)   
- Poverty headcount ratio at societal poverty line (% of population)
All data has been extracted on period of 10 years, from 2015 to 2024.

## Files available
`Poverty VS Government Expenditure_2015_2024_Data.csv` : CSV file containing indicators mentionned above, detailed by country and year  
`Poverty VS Government Expenditure.ipynb` : code for the project in a Jupyter Notebook  
`README.md` : Instructions to consult before starting project
  
## Installation
Please clone the GitHub repository before using it and feel free to do any improvment once done.  
```
$ git clone https://github.com/Nitrof78/Poverty_Ratio_VS_Government_Expenditure  
$ cd Poverty_Ratio_VS_Government_Expenditure
```

## Necessary libraries
For this project, we'll use the following libraries, first step of the project consists in importing them :  
- Pandas - Python Data Analysis Library  
- Matplotlib - Visualization with Python
- NumPy - Scientific computing with Python
- Scikit-learn - machine learning in Python
- Seaborn - Statistical data visualization

## Usage Guidelines
### Project structure
Project is deployed in a Jupyter Notebook. Steps have to be applied in chronological order.  
Datasource is a `CSV` file stored in the repository and named `Poverty VS Government Expenditure_2015_2024_Data.csv`. 
### Datasource update  
If you wish to change datasource, adding other indicators, changing time period, you'll have to respect a few rules :  
1) Data is coming from World Bank Databank Website https://databank.worldbank.org/source/world-development-indicators
2) You'll have to select 3 dimensions :
   - `Country` : You can select whatever country or region you want
   - `Series` : This is where you'll chose the indicators you want to use, be sure to select indicators with available value for the countries you want to study
   - `Time` : You can select a period of time of your choice
3) Once variables are selected, modify the layout to have a database compatible
   - `Time` and Country must be considered as 'Rows'
   - `Series` is considered as 'Column'
4) Then you can Download a file, chosing `CSV` file format
5) Store the Data CSV file in your repository and name it in a clear way
6) Modify step 2 of the Jupiter Notebook to take into account the name of your datasource
```ruby
#We load data from the csv file.  
df = pd.read_csv('YourFileNameHere.csv')
df.head()
```
Please note that, if you modified the indicators taken into account, several steps of data cleaning will also have to be updated.

## Current results
In its present configuration, the anlysis shows strongest (negative) correlation of poverty ratio with Education and Health Expenditure, without solving the question about wether Education and Health lead to less poverty, or if less poverty gives more latitude for Health and Education Expenditures. Some exploratory leads would be to study results by region or similar countries and use historical data to understand the link between the indicators and poverty ratio.

## License Type
All indicators are coming from one database, with the following license :  
  CC BY-4.0  
  https://creativecommons.org/licenses/by/4.0/  
Project in itself is a public work, designed to practice on World Bank Databank Website, feel free to clone it and improve it as you wish.
