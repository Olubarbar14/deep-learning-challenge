# deep-learning-challenge

# Report
------------------------------

## OVERVIEW:

###### Using my knowledge of pandas and scikit-learn, I performed preprocessing of charity_data.csv dataset.
###### I also compiled, trained, and evaluated the neural network model by using the features of the dataset
###### to create a binary classifier that can predict whether applicants will be successful if funded by
###### Alphabet Soup

# To accomplish this task, I performed the following steps:

## 1: Preprocess the Data

###### A: Read the csv file
![](images/load%20csv.png)

###### B: Drop the EIN and Name columns because they are neither targets or features
![](images/drop_ein_name.png)

###### C: Checked number of unique columns in DataFrame
![](images/unique_prepro.png)

###### D: Cutoff point to bin application and classification types
![](images/application_bin_prepro.png)
![](images/cutoff_appli_prepro.png)
![](images/cutoff_class_prepro.png)
![](images/cutoff_class_prepro2.png)

###### E: Coverted categorical data to numeric with pd.get_dummies
![](images/cutoff_prepro2.png)

###### F: Split my preprocess data into my features and target arrays
![](images/split_prepro.png)

## 2: Compile, Train, and Evaluate the Model
![](compile_prepro.png)
###### G: Created a callback that saves the model's weights every five seconds
![](images/callback_prepro.png)
###### H: Compile, train, evaluate
![](images/compile_prepro2.png)
![](images/compile_prepro3.png)
![](images/evaluate_prepro.png)
###### I: Saved  and exported results to HDF5 file

# 3: Optimized my Model 

## First Trial
###### J: Created a new jupyter notebook and performed the same preprocessing steps as above but added a third hidden layer
![](images/compile_opt1.png)
###### K: Evaluation show that only adding a third hidden layer did not reach the target predictive accuracy of 75% or higher
![](images/evaluate_opt1.png)

## Second Trial

###### L: Performed preprocessing again as in the steps above but this time only dropping the EIN
![](images/drop%20EIN.png)

###### M: Checked number of unique columns in DataFrame after dropping EIN
![](images/unique_after_ein.png)

###### N: Cutoff point to bin name, application and classification and Coverted categorical data to numeric with pd.get_dummies
![](images/cutoff_name.png)
![](images/cutoff_name_2_opt.png)
![](images/cutoff_application_opt.png)
![](images/cutoff_aplication_opt2.png)
![](images/cutoff_class_opt.png)
![](images/cutoff_class_opt2.png)

###### O: Split my preprocess data into my features and target arrays
![](images/split_opt.png)

###### P: Compiled, Trained, and Evaluated the Model and added a second instance of the sequential class to form another cluster layer
![](images/compile_opt.png)
![](images/compile_opt2.png)
###### Q: By removing just the EIN and adding a second sequential class, you can see the accuracy greatly improves and above the target 75%
![](images/compile_opt3.png)
![](images/evaluate_opt.png)

# Conclusion:
###### The final model with the NAME column added back in achieved an accuracy of 78% and a loss of 46%. Keeping the Name column was crucial
###### in achieving and and going beyond the target. This shows the importance of the shape of your datasets before you preprocess it. Deep learning
###### models with multiple layers are better since the model learns how to predict based on filtering inputs through layers












        

