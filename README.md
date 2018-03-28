# Seattle_Rainfall

#### The project aims to connect the environmental engineering background with the Python language.

#### 1.1 Data Extraction

   The Seattle Rainfall dataset is from kaggle: https://www.kaggle.com/rtatman/did-it-rain-in-seattle-19482017.
   
   It include daily data of max temperture, min temperture and rainfall from 1948-2017.
    
#### 1.2 Parameter Selection

   The probability is a kind of method to determine the possibility of an event occurring. A higher probability means that the event will happen more frequency.

   The probability of exceedance express the chance for a specified value being exceeded in a certain cycle. The equation for probability of exceedance, such as California, Weibull, Sevruk and Geiger are listed in the Table.

| Method             | Equation      | 
| ----------------   |:-------------:| 
| Weibull            | ![](https://latex.codecogs.com/gif.latex?p%3D%5Cfrac%7Bm%7D%7Bn&plus;1%7D )   |
| Sevruk and Geiger  | ![](https://latex.codecogs.com/gif.latex?p%3D%5Cfrac%7Bm-%5Cfrac%7B3%7D%7B8%7D%7D%7Bn&plus;%5Cfrac%7B1%7D%7B4%7D%7D)    |
| California         | ![](https://latex.codecogs.com/gif.latex?p%3D%5Cfrac%7Bm%7D%7Bn%7D)    | 
| Hazen              | ![](https://latex.codecogs.com/gif.latex?p%3D%5Cfrac%7Bm-0.5%7D%7Bn%7D)         |

   The return period build from probability of exceedance, it demonstrated the recurrence frequency for certain event. It is usually used for risk analysis to predict the hazard event.

   This project will use probability of exceedance to display the probability for each maximum precipitation in selected periods and use Weibull method to calculate the probability for each rainfall events. In addition, this project will construct the return period for Seattle.

#### 1.3 Model Selection

The project aims to build three Hydrology models and select the best model with Mean Square Error. Normal Distribution, Gumbel Distribution and Log Pearson Type III Distribution will be chosen in this project to build three models. Gumbel distribution methodology was selected to perform the flood probability analysis. Log Pearson Type III is statistical technique for fitting frequency distribution data to predict the design flood for a river at different site.

1. Normal Distribution

      ![](https://latex.codecogs.com/gif.latex?prep%20%3D%20avg%28prep%29%20&plus;%20z%5Ccdot%20%5Csigma_%7Bp%7D)

      ![](https://latex.codecogs.com/gif.latex?z%20%3D%20%5Cfrac%7Bx-avg%28prep%29%7D%7B%5Csigma%20_%7Bp%7D%7D)

2. Gumbel Distribution

      ![](https://latex.codecogs.com/gif.latex?prep%20%3Davg%28prep%29&plus;K%7B_%7BEV%7D%7D%5Ccdot%20%5Csigma%7B_p%7D)

      ![](https://latex.codecogs.com/gif.latex?K%7B_%7BEV%7D%7D%20%3D-%5Cfrac%7B%5Csqrt%7B6%7D%7D%7B%5Cpi%20%7D%5Ccdot%20%280.5572&plus;ln%28ln%5Cfrac%7BT_%7By%7D%7D%7BT_%7By%7D-1%7D%29%29%29)

3. Log Pearson Type III Distribution

      ![](https://latex.codecogs.com/gif.latex?log%28prep%29%20%3Dlog%28avg%28prep%29%29&plus;K%7B_%7BIII%7D%7D%5Ccdot%20%5Csigma%7B_%7Blog%28p%29%7D%7D)

      ![](https://latex.codecogs.com/gif.latex?K%7B_%7BIII%7D%7D%20%3D%5Cfrac%7B2%7D%7B%5Cgamma%7B_%7Blog%28p%29%7D%7D%20%7D%5Ccdot%20%28%28%28z-%20%5Cfrac%7B%5Cgamma%20_%7Blog%28p%29%7D%7D%7B6%7D%20%29%5Ccdot%20%5Cfrac%7B%5Cgamma%20_%7Blog%28p%29%7D%7D%7B6%7D%20&plus;1%20%29%5E%7B%5E%7B3%7D%7D-1%29)

#### 1.4 Result 
     
  Result is shown in the code in https://github.com/anyarcherty/Seattle_Rainfall/blob/master/Seattle%20Weather.ipynb

#### 1.5 Conclusion
   In this project, Log Pearson Type III model works well to find annual maximum rainfall in Seattle. For future research, my suggestion is to obtain enough precipitation data at different rainfall stations near Seattle and try to build precipitation intensity network in Seattle. Also, I suggest building the models based on the different data analysis models.
