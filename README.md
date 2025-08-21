# San Francisco Crime Classification
<img width="1600" height="867" alt="image" src="https://github.com/user-attachments/assets/61aec2e7-ae3c-442c-8cb9-bb3217983a80" />


# Description
From 1934 to 1963, San Francisco was infamous for housing some of the world's most notorious criminals on the inescapable island of Alcatraz.

Today, the city is known more for its tech scene than its criminal past. But, with rising wealth inequality, housing shortages, and a proliferation of expensive digital toys riding BART to work, there is no scarcity of crime in the city by the bay.

From Sunset to SOMA, and Marina to Excelsior, this competition's dataset provides nearly 12 years of crime reports from across all of San Francisco's neighborhoods. Given time and location, you must predict the category of crime that occurred.

We're also encouraging you to explore the dataset visually. What can we learn about the city through visualizations like this Top Crimes Map? The top most up-voted scripts from this competition will receive official Kaggle swag as prizes.


# Acknowledgements
Kaggle is hosting this competition for the machine learning community to use for fun and practice. This dataset is brought to you by SF OpenData, the central clearinghouse for data published by the City and County of San Francisco.

# Evaluation
Submissions are evaluated using the multi-class logarithmic loss. Each incident has been labeled with one true class. For each incident, you must submit a set of predicted probabilities (one for every class). The formula is then:

![multi-class_logarithmic_loss](https://github.com/JamesSuryaPutra/San-Francisco-Crime-Classification/assets/155945814/ca734c21-03d4-4c39-a540-cbb7bcbb6d28)


where N is the number of cases in the test set, M is the number of class labels, log is the natural logarithm, yij is 1 if observation i is in class j and 0 otherwise, and pij is the predicted probability that observation i belongs to class j.

The submitted probabilities for a given incident are not required to sum to one because they are rescaled prior to being scored (each row is divided by the row sum). In order to avoid the extremes of the log function, predicted probabilities are replaced with max(min(p,1−10−15),10−15).
