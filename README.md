# Credit Risk Report
## Report for credit risk analysis

>"Too big to fail"

In this report we will cover the purpose of our credit analysis, the artifical learning models used, and the findings of the models:

* The purpose of our investigation was to verify the number of healthy credit loans against the number of risky loans. 
* Our dataset was a local "lending_data" CSV file. 
* In this dataset we were looking for the "loan_status" indicators and the number of loans listed as either healthy ("0") or risky ("1")
* Initial steps for the data included importing the data into a Pandas dataframe for manipulation, 
  splitting the dataset into "training" and "testing" datasets for use in modeling, 
  and fitting the dataset to our Logistic Regression Model for predictions. 
  
* The dataset was imbalanced-- meaning it contained far more healthy loans ("0") than unhealthy. For the purposes of accurate modeling we resampled the dataset 
  such that the risky ("1") loans were evenly numbered against that of the healthy. This allowed for more accurate modeling with our Logistic Regression Model. 
  
## Results

* Machine Learning Model 1:
  * Below we will include an image with the results of the modeling for the original dataset. This dataset is imbalanced as has not yet been subjected to any resampling: 
  We can see that the model has a high degree of accuracy when detecting the healthy loans ("0") and a somewhat lessened, but still useful, degree of accuracy when detecting the risky loans.
  
  ![<alt text>](https://i.postimg.cc/TwfVCgDm/Screen-Shot-2022-07-07-at-11-51-40-AM.png)
     
* Machine Learning Model 2:
  * Below we will add an image the covers the accuracy scores for the secondary model used. This model took the dataset and resampled the risky loans ("1") so that they were of equal count 
    to those of the healthy ("0") loans. We can see that the resampled data fares a little better than the original dataset when it comes to detecting the risky ("0") loans. This difference  
    in value may seem small but may in itself warrant use of the resampled model. 
     ![<alt text>](https://i.postimg.cc/6QkMf8Wx/Screen-Shot-2022-07-07-at-12-03-29-PM.png)
   

## Summary

In this report we took our lending dataset, split the data into training and testing groups for modeling with a Logistic Regression Model in order to detect healthy ("0") and risky ("1") loan values. 
* Of the two models it appears that the resampled dataset model renders slightly better results when attempting to find and classify the risky loans. 
* Performance of the models does depend on what we are trying to solve for. In this case detecting the amount of fewer risky loans when compared to the overall dataset. 

    To that end the resampled model appears to track the risky ("1") data ever so slightly better than the original dataset and we will reccomend using this model. 
    
    
    