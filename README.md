# Industrial-Power-Demand-Dataset
The practical real-time power demand datasets named IPDD(Industrial-Power-Demand-Dataset) is collected form a steel plant, which consists of three-phase electric current, three-phase active power and three-phase demand active power of the entire plant, and the interval of this collected raw data is 30 seconds. 
This dataset is used in a research of ultra-short-term industrial power demand forecasting, and the work has been published on IEEE Trans. on Power System. It is appreciated to cite this paper if you like to use this dataset.
Mao Tan, Siping Yuan, Shuaihu Li, Yongxin Su, Hui Li, Feng He, Ultra-short-term industrial power demand forecasting using LSTM based hybrid ensemble learning, IEEE Trans. on Power System, 2019, doi:10.1109/TPWRS.2019.2963109
The structure of IPDD as follows:
```
├── testset
└── trainingset
```
###### original attributes in data collection 
Attributes|Description
------------- | -------------
Date | YYYY/MM/DD HH:MM:SS
T_DEM | Three-phase total power demand for present interval
A/B/C_CUR | Real-time current of phase A/B/C 
A/B/C/T_ACT | Three-phase total real-time active power of phase A/B/C
S_DEM | Three-phase recent power demand updated every second
Hour | 0 ~ 23 corresponds to 24 hour of the day
Month | 1 ~ 12 corresponds to January ~ December
Day of Week| 1 ~ 7 corresponds to Monday ~ Sunday

The original attributes in the dataset as shown in the table above, there are two observations about the power demand. Present power demand T_DEM, the value for the last completed interval, which is used to predict and compare with the maximum demand limit. Recent power demand S_DEM, which is the real time value measured by the field data acquisition meters, and which represents the trend in the near future.
###### trainingset
This is the raw data collected from May 4 to July 15, 2018. According to that the step size of the sliding time block for power demand is set to 1 minute, when using the trainingset to train model for Ultra-short-term industrial power demand forecasting, you could to sample the records of trainingset at 1 minute intervals.
###### testset
Ten testing datasets, which are randomly selected from the raw data collected from July 15 to August 9, 2018, not included in the training dataset. During the forecasting, you could to select the first m time-steps of the series at 1 minute intervals and then predict the power demand of the next n time-steps.
