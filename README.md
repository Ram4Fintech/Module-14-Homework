# Module-14-Homework

## Background and establishing a Baseline performance:
The scope of this work is to improve upon the already existing algorithmic trading environment by enhancing the trading signals with machine learning algorithms. To make this happen, the OHLCV data was read and imported into a Dataframe. Trading signals were generated using the short and long windows. Thereafter thew data were split into training and testing datasets. the training of the dataset was done for a selected period of 3 months. The SVM classifier model was then used to fit the training data and make predictions on the testing data. A classiofication report was prepared for checking accuracy, precision and recall
In completing this initial task, a DataFrame containing the Predicted values, Actual Returns and Strategy Returns was done and visualised with hvplot 

## Analysing the Baseline performance:
Based on the anaysis in this section it is fair to conclude as follows: 
In the beginning in 2015, the Strategy Returns were higher than the actual returns. IOn 2016, both the returns were equalising as the curves crosed each other. But since then the Actual Returns have been higher than the Strategy Returns. 
Between 2016 and 2019, there was an indirect corelation between the two, that is Actual Returns were increasing whereas the Strategy Returns were decreasing. In the first quarter of 2020, both the curves took a steep drop, possibly due to Covid(?). Thetreafyer there was a direct corelation for about 6 months till the 3rd quarter of 2020 when the both the returns shopwed an increase, but since then till 202a1, Actual Returns have ioncreased sharply whereas the Strategy Returns have started to fall. Please refer to the plot here![Alt text](<Fig 1 - Actuals vs Strategy Returns.png>):
 
 ## Step 1: Tuning the Baseline Algorithm with an adjusted size of training dataset to 6 months instead of 3 months in the baseline as above:
 This tuning of the dataset resulted in a slightly different result in the first six months. As you could see in the image below and as compared to the previous image, the Actual Returns did not fall below the Strategy returns at all here as was noticed in the previous one with 3 months period. In the 6 months one, the Actual Returns have started rising even earlier in the beginning of 2016 as opposed to the end of quarter 1 of that year 2016.
 Therefore the conclusion is that more the training dataset offset period, better results emerge. Please refer to the plot here:![Alt text](<Fig 2 - Actuals vs Strategy Returns with a 6 months Dateoffset finetuning of the training dataset.png>)

## Step 2: Tuning the Baseline algorithm by changing the SMA input features:
The SMA input features were changes as follows - short_window from 4 to 20 and long_window from 100 down to 80. The notebook was rerun to the end. The resultant comparison of the plot was not any different to the original baseline one. Please refer to the plot here: ![Alt text](<Fig 3 - Actuals vs Strategy Returns with varied SMA input features finetuning of the training dataset.png>)
Therefore it's fair to conclude that changing both the SMA input features has not made any changes to the outcomes

## Step 3: Tuning the Baseline alogorithm to get the best outcome:
I made the following chaqnges: The SMA short_window was changed to 10 and the long_window to 50. In addition, the ending period of thew training dataset was changed with an offset of 12 months. After re-running all the cells, this appears to give a better Actual result in the bewgiining months of 2016 as conmpared to Steps 1 and 2. Please refer to the plot here: ![Alt text](<Fig 4 - Actuals vs Strategy Returns  finetuning for the best outcome.png>)

## Evaluating with Logistic Regression classifier:
The Logistic Regression model was imported and then the original data was fitted with this new classifier. This was then backtested for its performance. A new dataframe was created withg the predictions and this was also visualised with an hvplot. The conclusion with this is that this outcome is very simialr to the outcome in the Baseline algorithm. There is only a very marginal difference in accuarcy and precision. Visually the plots also look pretty much the same