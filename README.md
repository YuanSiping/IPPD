# Industrial-Power-Demand-Dataset
The practical real-time power demand datasets named Industrial-Power-Demand-Dataset(IPDD) is collected form a steel plant, which consists of three-phase electric current, three-phase active power and three-phase demand active power of the entire plant, and the interval of this collected raw data is 30 seconds. The structure of IPDD is as follows:
```
├── testset
└── trainingset
```
###### trainingset
This is the raw data collected from May 4 to July 15, 2018. According to that the step size of the sliding time block for power demand is set to 1 minute, it could to sample the records of raw data at 1 minute intervals.
###### testset
Ten testing datasets, which are randomly selected from the raw data collected from July 15 to August 9, 2018, not included in the training dataset.
