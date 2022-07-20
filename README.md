# Seattle_Airbnb_Udacity
This repository is being created to analyze Seattle Airbnb Udacity.

Published Blog Link - https://medium.com/@amanchawla9793/f876f4203451


- Installations
- Project Motivation
- File Descriptions
- Structure of the code


</br>



<b>Installations</b>
- import pandas as pd
- import numpy as np
- import math
- import matplotlib.pyplot as plt
- %matplotlib inline
- import seaborn as sns

- from folium import Map
- from folium.plugins import HeatMap
- import folium

- from sklearn.linear_model import LinearRegression
- from sklearn.model_selection import train_test_split
- from sklearn.metrics import r2_score, mean_squared_error, mean_absolute_error

</br>

<b>Project Motivation</b>
- Seattle is one of the largest metropolis of the Pacific Northwest, and one of the largest and most affluent urban centres in the United States. Seattle is famous for Starbucks and overall coffee culture, grunge music scene, the Seahawks, the Space Needle, Pike Place Market, headquarters of a lot of the tech industry (including both Amazon and Microsoft), hiking, kayaking, and general outdoors lifestyle.
- Since it is one of famous tourist destination in U.S, this is elaborative data for Seattle's all Airbnb bookings and property for year 2016 and lot of business questions can be answered from this data.
- For example some new property want to list their property and want to understand how property should be priced and what factors can affect price, this dataset can be used to get some useful insights.
- Another useful utility for this dataset can be for someone who want is looking to enter hospitality business and want to understand what are the hot locations and what location have potential to be next hot location and what are the amenities and type of property that can get more price and occupancy.


</br>



<b>File Descriptions</b>

The following Airbnb activity is included in this Seattle dataset:
-	Listings, including full descriptions and average review score
-	Reviews, including unique id for each reviewer and detailed comments
- Calendar, including listing id and the price and availability for that day

</br>

<b>Structure of the code</b>

In the Jupyter notebook CRISP-DM Process (Cross Industry Process for Data Mining) approach has been followed.


<!DOCTYPE html>
<html>

<body>
	<table>
		<thead>
			<tr>
				<th><span style="font-size:10.5pt;line-height:107%;
font-family:&quot;Helvetica&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;;
color:black;mso-ansi-language:EN-IN;mso-fareast-language:EN-IN;mso-bidi-language:
AR-SA">S No</span><br></th>
				<th><span style="font-size:10.5pt;line-height:107%;
font-family:&quot;Helvetica&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;;
color:black;mso-ansi-language:EN-IN;mso-fareast-language:EN-IN;mso-bidi-language:
AR-SA">Steps</span></th>
				<th><span style="font-size:10.5pt;line-height:107%;
font-family:&quot;Helvetica&quot;,sans-serif;mso-fareast-font-family:&quot;Times New Roman&quot;;
color:black;mso-ansi-language:EN-IN;mso-fareast-language:EN-IN;mso-bidi-language:
AR-SA">Approach</span></th>
			</tr>
		</thead>
		<tbody>
			<tr>
				<td>&nbsp;1</td>
				<td>&nbsp;Business understanding</td>
				<td><p class="MsoNormal"><span style="font-size:10.5pt;line-height:107%;font-family:&quot;Helvetica&quot;,sans-serif;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-fareast-language:
EN-IN">Objective of the analysis is to get insights which can help current host
and any new host that want their property listed in Airbnb.<o:p></o:p></span></p>
<p class="MsoNormal"><span style="font-size:10.5pt;line-height:107%;font-family:&quot;Helvetica&quot;,sans-serif;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-fareast-language:
EN-IN">Some of questions that would be answered in this project are:<o:p></o:p></span></p>
<p class="MsoNormal"><span style="font-size:10.5pt;line-height:107%;font-family:&quot;Helvetica&quot;,sans-serif;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-fareast-language:
EN-IN">What time of year demand for accommodation is highest?<o:p></o:p></span></p>
<p class="MsoNormal"><span style="font-size:10.5pt;line-height:107%;font-family:&quot;Helvetica&quot;,sans-serif;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-fareast-language:
EN-IN">What factors affect the pricing of the property?<o:p></o:p></span></p>
<p class="MsoNormal"><span style="font-size:10.5pt;line-height:107%;font-family:&quot;Helvetica&quot;,sans-serif;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-fareast-language:
EN-IN">What type of property have potential to grow and provide business opportunity
in Seattle?<o:p></o:p></span></p>
<span style="font-size:10.5pt;line-height:107%;font-family:&quot;Helvetica&quot;,sans-serif;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-ansi-language:EN-IN;
mso-fareast-language:EN-IN;mso-bidi-language:AR-SA">What location in Seattle have
highest and lowest competition?</span>&nbsp;</td>
			</tr>
			<tr>
				<td>&nbsp;2</td>
				<td>&nbsp;Data Understanding</td>
				<td>&nbsp;Calendar file have insights such as:<p class="MsoNormal"><span style="font-size:10.5pt;line-height:107%;font-family:&quot;Helvetica&quot;,sans-serif;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-fareast-language:
EN-IN">What is occupancy for each property and for each month?<o:p></o:p></span></p>
<p class="MsoNormal"><span style="font-size:10.5pt;line-height:107%;font-family:&quot;Helvetica&quot;,sans-serif;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-fareast-language:
EN-IN">&nbsp;</span></p>
<p class="MsoNormal"><span style="font-size:10.5pt;line-height:107%;font-family:&quot;Helvetica&quot;,sans-serif;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-fareast-language:
EN-IN">Listing Column have insight such as:<o:p></o:p></span></p>
<p class="MsoNormal"><span style="font-size:10.5pt;line-height:107%;font-family:&quot;Helvetica&quot;,sans-serif;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-fareast-language:
EN-IN">What numeric and categorical variables have strong relation with price?<o:p></o:p></span></p>
<p class="MsoNormal"><span style="font-size:10.5pt;line-height:107%;font-family:&quot;Helvetica&quot;,sans-serif;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-fareast-language:
EN-IN">What location in Seattle have highest property density? <o:p></o:p></span></p>
<span style="font-size:10.5pt;line-height:107%;font-family:&quot;Helvetica&quot;,sans-serif;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-ansi-language:EN-IN;
mso-fareast-language:EN-IN;mso-bidi-language:AR-SA">What amenities have highest
impact with price?</span></td>
			</tr>
			<tr>
				<td>&nbsp;3</td>
				<td>&nbsp;Prepare Data</td>
				<td>&nbsp;Columns with strong relationship with Price are selected for further modelling<br>
<span style="font-size:10.5pt;line-height:107%;font-family:&quot;Helvetica&quot;,sans-serif;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-ansi-language:EN-IN;
mso-fareast-language:EN-IN;mso-bidi-language:AR-SA">Columns with missing value
are filled using appropriate method</span></td>
			</tr>
			<tr>
				<td>&nbsp;4</td>
				<td>&nbsp;Data Modeling</td>
				<td>&nbsp;Linear Regression model has been designed to do price prediction</td>
			</tr>
			<tr>
				<td>&nbsp;5</td>
				<td>&nbsp;Evaluate the Results</td>
				<td>&nbsp;There are 3 main metrics for model evaluation in regression:<p class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
line-height:normal"><span style="font-size:10.5pt;font-family:&quot;Helvetica&quot;,sans-serif;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-fareast-language:
EN-IN">1. R Square/Adjusted R Square<o:p></o:p></span></p>
<p class="MsoNormal" style="mso-margin-top-alt:auto;mso-margin-bottom-alt:auto;
line-height:normal"><span style="font-size:10.5pt;font-family:&quot;Helvetica&quot;,sans-serif;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-fareast-language:
EN-IN">2. Mean Square Error(MSE)/Root Mean Square Error(RMSE)<o:p></o:p></span></p>
<span style="font-size:10.5pt;line-height:107%;font-family:&quot;Helvetica&quot;,sans-serif;
mso-fareast-font-family:&quot;Times New Roman&quot;;color:black;mso-ansi-language:EN-IN;
mso-fareast-language:EN-IN;mso-bidi-language:AR-SA">3. Mean Absolute Error(MAE)</span></td>
			</tr>
		</tbody>
	</table>
</body>
</html>
