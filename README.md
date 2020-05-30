# Udacity Capstone Challenge - Starbucks

## Motivation
The goal of this analysis is to perform exploratory data analaysis, 
define a metric to measure customer response to different promotional offers and 
build a machine learning model to predict customer response based on 
customer socio-demographic attributes and offer attributes.

## File description
* data [folder] - folder containing data analysed
  * portfolio.json - simulated Starbucks offer attributes
  * profile.json - simulated Starbucks offer app customer profiles
  * transcript.json - simulated transaction and offer events transcript
* Starbucks_Capstone_final.ipynb [file] - Jupyter Notebook containing exploratory data analysis and model

## Summary

In summary, I took the events of members receiving informational, bogo and discount offers and augmented these events with additional dimensions - customer socio-demographic attributes and offer attributes (type, difficulty, reward, and duration).

I then defined and calculated a binary response metric, which for bogo and discount offers indicates if customers received, viewed and completed an offer (all within the offer validity period) or if they failed to view or complete an offer. For informational offers, I calculated a very simple and optimistic response metric, assuming that any transaction made during the duration of the informational offer is sufficient for “completion”.

Having merged the receive-respond datasets for bogo, discount and informational offers, I performed simple data exploration and found that the only targeting Starbucks performs in sending promotion offers is related to income cohorts - med-high and high income customers receive more offers than low and medium income customers.

I also found that female, higher income, older, and long-term app users respond marginally better to all offers.

Armed with this knowledge, I have fit several classification models to predict if a customer would respond to any given offer and selected RandomTreeClassifier as the best model. I attempted hyperparameter tuning to improve model accuracy, but there was no improvement and my final model showed an F1 score of 0.65.


## Links
[Link to Medium Post](https://medium.com/@arunas.umb/starbucks-capstone-challenge-predicting-response-to-promotions-with-ml-70284b64d297?sk=b793f28fb1911a14dc7ab2511641174f)
