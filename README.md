# Seattle_Rainfall

#### This project aim to connect the Environmental Enginnering backgroud with Python Language.

1.1 Data Extraction

   The Seattle Rainfall dataset is from kaggle: https://www.kaggle.com/rtatman/did-it-rain-in-seattle-19482017.
   
   It include daily data of max temperture, min temperture and rainfall from 1948-2017.
    
1.2 Parameter Selection

   The probability is a kind of method to determine the possibility of an event occurring. A higher probability means that the event will happen more frequency.

   The probability of exceedance express the chance for a specified value being exceeded in a certain cycle. The equation for probability of exceedance, such as California, Weibull, Sevruk and Geiger are listed in the Table.

| Method             | Equation      | 
| ----------------   |:-------------:| 
| Weibull            | <img src="https://latex.codecogs.com/svg.latex?\Large&space;p=\frac{m\pm\n+1} title="\Large p={x\pm\n+1" />" |
| Sevruk and Geiger  | centered      |
| California         | are neat      | 
| Hazen              |                 |
The return period build from probability of exceedance, it demonstrated the recurrence frequency for certain event. It is usually used for risk analysis to predict the hazard event.

This project will use probability of exceedance to display the probability for each maximum precipitation in selected periods and use Weibull method to calculate the probability for each rainfall events. In addition, this project will construct the return period for Seattle.

1.3 Model Selection

The project aims to build three Hydrology model and select the best model with Min Mean Square Error.
