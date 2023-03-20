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

![](BOV,OVA,POT-new.png)

### WF,IR,SM Column Cleaning
In this section,it was noticed that a character in the form of a bold star was scraped with the file,and it was my duty to remove the string character that was alongside the value.To perform this tranformation,in my Power Query editor,in the Add Column bar,i reached for the Column from Example icon in other to do the transformation.Below is the Before and After transformation,and of course:sunglasses:i renamed my column header for easy identification.


![](WF,IR,SM.png)

![](WF,IR_SM-new.png)


### Contract Column Transformation
The data cleaning process that was carried out in this section was in different categories.The contract column contained contract start year and end year,informations about the number of years the player spent in the club,and the agreement that each player was under in the club.Below is an image representing what it looked like.

![](Agreement_example.png)

Afterwards,an **Agreement** column was the first transformation that was made.The agreement column was created using an **M-Language**

if Text.Contains([Contract], "Free") then 
    "Free" 
else if Text.Contains([Contract], "Loan") then 
    "Loan" 
else 
    "Contract"
    
 Below, is the interpretation of the **M-Language**
 
 ![](Agreement_new.png)
 
 The second transformation that was made was on the **Duration** column which also was done using an **M-Language**
 
 if Text.Contains([Contract], "~") then
    Number.From(Text.AfterDelimiter([Contract], "~")) - Number.From(Text.BeforeDelimiter([Contract], "~"))
else
    0
    
 Below, is the response to the above **M-Language**
 
 ![](Duration.png)
 
 Finally:tired_face:to get our Sign in Year and Signed out Year,i used the Split column by Delimiter fuction. Which allows you to split column using several characters.The character i wanted was not given,so i used the Custom character and specified it '~'
 

Here is the transformation:point_down:

![](Sign-in_Sign-out.png)


### Hits Column Transformation
In this column, there were values containing the letter "K"(1.6K) instead of 1600.To achieve this, i removed the value K, and multiplied the remaining values by 1000 
 
Here is an image of what it looked before
 

