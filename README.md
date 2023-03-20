# FIFA21-Data-Cleaning

![](fifa-image_.jpg)

## Introduction
This is a power BI project which involves the documentation of different **Fifa Players** Worldwide obtained from Kaggle datasets.The data transformation was done in the 
Power query editor. The first step was to get the Data, which prompted me on various ways in which i wanted to get my data. The dataset is in a CSV format which i clicked on and immediately took me to an interface, thereafter i transformed my data into my Power query editor. The dataset contained several column headers that was abbreviated e.g OVA as Overall rating,IR as injury rating,Long name as Players_name and many others. The first transformation that was done was to check the Data dictionary that was provided and i renamed the headers. The dataset contained about 18,979 rows and 76 column headers after transformation. Now lets begin:smiley:

### Photo **URL** Correction
The dataset contained a column that displays the link to the image of each player. I noticed that when i click on the link and go to my browser the image is not displaying. so, the first transformation that was done was to look for the appropraite link through the player url that was provided to correct that error. Here is the link to what it was like before https://cdn.sofifa.com/players/158/023/21_60.png The new link to what it is like now after making data cleaning is below https://cdn.sofifa.net/players/158/023/21_240.png


![](Photo_url-new.png)

### BOV,OVA,POT Cleaning
In this section,it was noticed that data that was supposed to be in percentages,were recorded in text.The transformation that was done as regards this was to first divide the values by 100,after then we can convert it to pecentages.In the Power Query editor,under the Transform tab locate the Standard box and then divide the values given,then you have your answer:relieved: 
Below is the images before and after transformation.


![](BOV,OVA,POT.png)

![]()
