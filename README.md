# eDreams test for Data Scientist Role

Repository of the test for the Data Scientist position in eDreams.

## PREDICTING BAGGAGE LIKELIHOOD

### OVERVIEW

At eDreams ODIGEO we are always looking for ways to improve customer satisfaction. With this objective in mind, we would like to predict whether a new customer is interested in buying additional baggage in order to speed up the booking process.

### GOAL

The goal of this task is to predict which new customers are going to purchase additional baggage for their trips using historical information from past bookings. The code can be developed in any of the following languages: Python, R or Java.

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

### GENERAL GUIDELINES

- It is up to you to submit the solution in the format you prefer (markdown, html, jupyter notebook, shiny report, etc). Nevertheless, if the submitted files consist only in code and comments, and you plot your graphics on the side during the exploration, please include these in a folder so that they can be referenced.
- Every decision (what steps are taken, what algorithms are used, what data is transformed or discarded) should have a succinct explanation or justification.
- We are looking forward to knowing how much you know about the context (problem, possible solutions, repercussions) at every step of the data science flow. Show us the best you can do at each of the steps and why: data cleaning, transformations, validations, modeling, tuning, etc.

### EVALUATION

The evaluation will be based on the quality and explanation of the source code, analysis performed, insights extracted and comments as well as the prediction scores. For the prediction score, the metric will depend on the output: in case a binary output is submitted, the evaluation method will be the F1 Score, in case a probability is given, the evaluation method will be the AUC ROC. If you consider there is also other interesting metrics to evaluate the exercise feel free to add them.

### SUBMISSION FORMAT

The submission must contain the source code and the predictions for the 30000 bookings in
CSV (Comma Separated Values) format, for instance: <br>

`ID EXTRA_BAGGAGE`: {0 True, 1 False} <br>
Or the probabilities: <br>
`ID EXTRA_BAGGAGE`: {0 0.35, 1 0.78}
