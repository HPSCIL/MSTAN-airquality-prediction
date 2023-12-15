
# MSTAN 

### Predicting air quality with a multi-scale spatio-temporal attention network ###

<font face="Times new roman" size=4>
This repo is the implementation of our manuscript entitled Predicting air quality with a multi-scale spatio-temporal attention network. The code is based on Pytorch 1.12.1, and tested on a GeForce RTX 4090 GPU with 24GB memory.


In this study, we present an attention-based approach   for air quality prediction at multiple monitoring stations termed the Multi-scale Spatio-Temporal Attention Network (MSTAN). Experiments with two real-world datasets showed the proposed MSTAN achieved the highest prediction accuracies for 12,18 and 24-hour prediction time lengths, compared to several state-of-the-art methods.

## Framework

![MSTAN](./Fig/MSTAN.png)


## Requirements
MSTAN uses the following dependencies
 
- Pytorch 1.12.1 and its dependencies
- Numpy and Pandas
- CUDA 11.8 or latest version

<<<<<<< HEAD
## Dataset
We list PM2.5 data for 35 monitoring stations in Beijing from January 1, 2017, to March 27, 2018. In addition, we have provided information on five auxiliary meteorological factors (temperature, humidity, pressure, wind speed, and wind direction). The Beijing_PM2.5 data can be aquired by [here](./MSTAN/Data/Beijing_PM25_raw.xlsx) 

We list AQI data for seven air quality monitoring stations in Tianjin from January 1, 2016, to December 31, 2017, excluding any additional auxiliary forecast data.The Tianjin_AQI data can be aquired by [here](./MSTAN/Data/Tianjin_AQI.xlsx) 


=======
>>>>>>> 882af7123ee9f4ddc6a50c9898f0e3ca1b3724ef
## Folder Structure
We list the code of the major modules as follows:<br>
- The main function to train/test our model: [click here](./MSTAN/code/main.py)<br>
- The source code of our model: [click here](./MSTAN/code/model/MSTAN.py)<br>
- Train and test data preporcessing are located at: [click here](./MSTAN/code/utils/pro_data.py)<br>
- Metric computations: [click here](./MSTAN/code/utils/All_Metrics.py)<br>

## Arguments
We introduce some major arguments of our main function here.

Training settings:
- train\_rate: rate of train set<br>
- test\_rate: rate pf test set<br>
- lag: time length of hidtorical steps<br>
- pre\_len: time length of future steps<br>
- num\_nodes: the number of stations<br>
- batch\_size: training or testing batch size<br>
- input\_dim: the feature dimension of inputs<br> 
- output\_dim: the feature dimension of outputs<br>
- learning\_rate: the learning rate at the beginning<br>
- epochs: training epochs<br>
- early\_stop_patience: the patience of early stopping<br>
- device: using which GPU to train our model<br>
- seed: the random seed for experiments<br>

Model hyperparameters:<br>
- d\_model: position encoding embedding dimension<br>
- cheb\_k: Chebyshev polynomials order<br>
- block1\_hidden: number of hidden layers in the first block<br>
- block2\_hidden: number of hidden layers in the second block<br>
- time\_strides: time resolution<br>
- nb\_block: number of Multi-Spatio-Temporal_Block (MST\_Block)<br>
- dropout: dropout rate<br>


## Citation
To Cite MSTAN in Publications<br>
- A paper describing MSTAN will be submitted to a scientific journal for publication soon<br>
- For now, you may just cite the URL of the source codes of MSTAN (https://github.com/HPSCIL/MSTAN-airquality-prediction) in your publications</font>


