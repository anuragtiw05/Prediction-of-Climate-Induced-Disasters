# CLIMATE_INDUCED_DISASTERS:-

We used deep learning methods to predict disasters.

#AIM and brief work TIMELINE:-

The project aims to predict climate-induced disasters and floods using machine learning and deep learning models. 
We attempted to obtain the similar parameters used in the paper and apply them to the Indian scenario in the state of Kerala. Since the dataset was maximum for Kerala,it was preferred. 
Although with sufficient training data, any region of India could be used. 

#IMPLEMENTATION:-

Now there were many parameters used in the paper, but we decided to use the following set of parameters :-

●	DTR (Daily Temp Range)- this was the parameter which depicted the extremism of the weather and is relevant in the flood scenarios.
●	CWD-this parameter related to rainfall and thus was important to consider.
●	TN10p
●	TX10p         
Some parametrs like FROST DAYS were irrelavant for KERELA as its temperature never drops below 0 so no point of counting days below 0C.  

1)	DTR (daily temperature range) (Expert Team on Climate Change Detection and Indices 2009; Wazneh, Arain and Coulibaly 2017) represented by Eq. 1, where TXij and TNij are the daily maxima and minimum temperature, respectively, on day i in period j.
2)	CWD (maximum length of the wet spell) (Expert Team on Climate Change Detection and Indices, 2009; Wazneh et al. 2017) which is calculated by counting the largest number of consecutive days where RRij≥1 mm, where RRij is the daily precipitation amount on day i in period j.
3)	TN10P (Expert Team on Climate Change Detection and Indices 2009; Wazneh et al. 2017) refers to the percentage of days when TNij<TNin10, where TNij is the daily minimum temperature on the day i in period j and TNin10 is the calendar day 10th percentile centred on a 5-day window for the base period 1961–1990.
4)	TX10p: Percentage of days when TX<10th percentile. Now, for calculating these parameters’ python was used and the codes will be attached below. Also, the use of excel was done.

#EXPANSION OF OUR WORK:-

For this ,first one needs to get the historic data from one of the The 12 Global climate models and needs to assume the RCP = 2.6 for data of year>2014.
Now one needs to decide the timeline in which one is working like we worked on 1985 to 2014 so we made a separate excel file for these years of Tmax , Tmin , precipitation.
Then one has to select the regions and also should have the iunformation about whether there was flood in that region int hat specific year or not and also have to select the regions where there was no flood for y=0 points also.
**We have also uploaded our final excel file which contained the values of features and the locations and both flood and non flood points.
#DTR:-
It is calculated annually and for that say one needs to calculate the DTR FOR 2010 , select the enteries of 2010 in both Tmax and Tmin then take the difference and then average using the inbuild functions in excel.

#CWD:-
**The code for cwd is given in the colab notebook , "CWD.ipynb".

#TN10p and TX10P:-
For this first select the base period for which you want to calculate the features , we selected 1985-2014 as our base period and then per day values were stored in a excel file using the code then we took the average for the whole year and calculated the value.
**The code for cwd is given in the colab notebook , "1985-2014.ipynb".

#Final prediction:-

We then filled the excel file with the 4 features of a specific location and the 5th feature was whether there was flood in that location in that year or not thats why we calculated all the features annually.
Now there are 4 input features and 1 output feature.
Apply the binary classification models like logistic regression , random forest , XGBoost Classifier , etc,.
**We have uploaded a notebook where we have made the predicitons using different models and also calculated the p-values and correlations in "flood_prediction.ipynb".
