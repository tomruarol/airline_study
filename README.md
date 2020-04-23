# Airlane Data Study

Complete Data Science flow for airlane data. 

From data import, feature engineering, to modeling and submission.

## PREDICTING BAGGAGE LIKELIHOOD

### GOAL

The goal of this task is to predict which new customers are going to purchase additional baggage for their trips using historical information from past bookings.

### DATA DESCRIPTION

Two files are attached with the training and test datasets. The training dataset contains 50,000 bookings and the test dataset 30,000 bookings. The data fields are the following ones: <br>

`TIMESTAMP`: (date) date when the booking was bought. <br>
`WEBSITE`: (string) Website where the trip was purchased. It is composed of a prefix that stands for the website (“ED” = Edreams, “OP” = Opodo, “GO” = Go Voyage) and a suffix for the country (for example: ES = Spain)<br>
`GDS`: (integer) Number of flights bought through the Global Distribution System <br>
`NO GDS`: (integer) Number of flights bought through other channels. <br>
`DEPARTURE`: (date) Departure date <br>
`ARRIVAL`: (date) Arrival date <br>
`ADULTS`: (integer) Number of adults <br>
`CHILDREN`: (integer) Number of children <br>
`INFANTS`: (integer) Number of infants <br>
`TRAIN`: (boolean) Whether the booking contains train tickets or not <br>
`DISTANCE`: (float) Distance travelled <br>
`DEVICE`: (string) Device used for the purchase <br>
`HAUL TYPE`: (string) Whether the trip was “Domestic”, “Continental” or “Intercontinental”.<br>
`TRIP TYPE`: (string) Trips can be either “One Way”, “Round Trip” or “Multi-Destination” <br>
`PRODUCT`: (string) Bookings can contain only travel (“Trip”) or travel and a hotel (“Dynpack”). <br>
`SMS`: (boolean) Indicates if the customer has selected a confirmation by SMS <br>
`EXTRA BAGGAGE`: (boolean) Variable to predict, only in the train dataset. Indicates if the customer has purchased extra baggage for the trip or not.

### EVALUATION

The evaluation method will be the F1 Score, in case a probability is given, the evaluation method will be the AUC ROC.

### SUBMISSION FORMAT

The submission must contain the source code and the predictions for the 30000 bookings in
CSV (Comma Separated Values) format, for instance: <br>

`ID EXTRA_BAGGAGE`: {0 True, 1 False} <br>
Or the probabilities: <br>
`ID EXTRA_BAGGAGE`: {0 0.35, 1 0.78}
