# Portfolio_Builder_Algo_Trading_Platform
This tool helps build, compare, backtest, benchmark and simulate porfolio returns based on style factors, sector or different Indexes with choice to either run in the background or in an interactive way providing a wizard at every step for the advisor to analyze the visualizations and calibrate Trading strategies

## Environment Requirements:
1. Bactesting.py for configuring SMA cross over strategy and running backtest
2. HVPlot for pandas, pyplot, holoviews and Matplotlib.
3. Entire User interface was developed using Panel Widgets. Panel module and ploty graph objects are to be installed and imported
4. API keys and database user name & pswd in .env file. alternately, these are to be entered in the respective fields on the GUI when pulling from different sources. 

## PROJECT PROPOSAL

1. Create a user interface / financial tool that allows us to loop through the SP 500 historical data that will allow us to generate a list of 10 stocks that have outperformed the index over a selected time frame ( 6months , 1yr, YTD, 5yr, 10 yr) and display the information on a graph with their individual performance compared to the benchmark (SP500) and the other 9 stocks. <br>

<u> Approach: </u> This was achieved via sector analysis for the given time frame. A python module names group4_project1_copy1.py accomplishes this tasks,
portraying visualizations indicating the sector performance as well as top performing stocks.<br>

2. Pull the financial metrics from the list (i.e. beta, eps, volume, etc)  to create a data base that we can use to enter a combination of any other 10 stocks from the SP500 to run a comparison<br>

<u> Approach: </u> from the sector analysis, a list of stocks can be picked and analyzed against different metrics such as beta, volume, etc., 
for each of the stocks picked, either real time data or historical data can be pulled using API or any data that is previously stored in csv files or in the database. this tool provides an option to store the data in local database (e,g PostGresql) eliminating the round trips everytime the user would like to analyze via visualizations<br>

3. Back test the model (generate financial metrics that led them to outperform the market)<br>

<u> Approach: </u> Using Backtesting.py module, the downselected stocks can be configured with single moving average or double moving average cross over strategies, with ability to set the slow/fast windows, initial investment, commission and other parameters. An Integrated plot showing the buy/sell signals, equity, P&L and other metrics is plotted to analyze and fine tune the backtesting strategy.<br>

4. If successful, implement the model using real time data for use during market hrs<br>

<u> Approach: </u> 

At Present the Tool enables to load the data upto the last hour. The next version of the tool will incorporate streaming data as against loading available data sets using APIs which usually has a lag.  <br>

<table>
<tr>
<td> 

![Initializer](/Resources/images/initializer.PNG) 

</td> 
<td> 

![Load Datafiles](/Resources/images/load_local_files.PNG)  

</td> 
</tr>
<tr>
<td>

![load API Data](/Resources/images/load_api_data.PNG)  

</td> 
<td>

![load Database](/Resources/images/load_database.PNG)   

</td> 
</tr>
<tr>
<td>

![Sector Analysis](/Resources/images/sector_analysis.PNG)   

</td> 
<td>	

![1 Year Top Sectors](/Resources/images/01Year_Sectors.png)
</td> 
<td>
</tr>
<tr>
<td>

![6 Months top Stocks](/Resources/images/6Month_TopStocks.png)
</td> 
<td>

![1 year Top Stocks](/Resources/images/1Year_TopStocks.png)
</td> 

</tr>
<tr>
<td>

![side by Side stock analysis](/Resources/images/side_by_side.PNG)  

</td> 
<td>

![configure BackTest](/Resources/images/configure_backtest.PNG)   

</td> 
</tr>
<tr>
<td>

![create custom visualizations](/Resources/images/dynamic_plot_gen.PNG) 

</td> 
</tr>
<tr><td>

![BackTesting](smacross.htm)
</td>
</tr>
</table>
