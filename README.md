# Man City vs Brighton Prediction

This project contains a notebook that predicts the total number of goals scored in a match between Manchester City and Brighton & Hove Albion. The code uses historical match data, including expected goals (xG) and other relevant metrics, to build a regression model to forecast the total goals.

## Data Collection

The data was manually collected from [FBref](https://fbref.com/en/), a site providing football statistics. The dataset includes metrics such as:

- **Home Expected Goals (xG)**
- **Away Expected Goals (xG)**
- **Home Expected Goals Against (xGA)**
- **Away Expected Goals Against (xGA)**
- **Total Goals Scored in the match**
- **Man City’s Home Points (repeated across matches)**
- **Brighton’s Away Points (repeated across matches)**

The actual number of goals scored in the game between Man City and Brighton was 4, and the over/under for total goals was set at 3.5, making this prediction model a good value for that specific match. The code was created and executed prior to the game, showing the model's accuracy.

## Approach

### Code Overview:

The project consists of two major parts:

1. **Data Preparation and Model Training**:
   - Features are selected from the collected data, including home and away xG, home and away xGA, as well as the total points for both teams in their respective home/away matches.
   - A **Gradient Boosting Regressor** model is used to predict the total goals in a match based on the selected features.
   - The data is split into training and testing sets, and the model is trained on the training data and evaluated on the testing data.

2. **Prediction for a New Match**:
   - A prediction is made for a future match using pre-defined xG and xGA values.
   - This prediction can be used to assess whether the over/under on total goals is good value based on historical performance and the model's output.

### Key Metrics:
- **Root Mean Squared Error (RMSE)**: 0.7318
- **R-squared**: -0.3389
- **Cross-validation (CV) Mean RMSE**: 0.6279

### Results:
- The model shows its predictions for the test data, including actual goals and predicted goals, helping to assess model performance.
- **Predicted total goals for tomorrow's match**: 4.0

### Explanation of the Second Code:
In the second code, additional data was included to account for the **Home and Away points for each team**. The total points for both Manchester City at home and Brighton away are added as extra features, which could provide more insights into the prediction model, potentially improving the accuracy.

## Conclusion

The notebook demonstrates how a machine learning model can be used to predict the total number of goals in a football match, based on relevant historical data such as xG, xGA, and team performance metrics. The model can be applied to other matchups as well, with potential improvements based on additional features or more advanced models.

## License

No license provided.
