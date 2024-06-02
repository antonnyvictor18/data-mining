# Favorita Store Sales Prediction

This project aims to predict sales for the thousands of product families sold at Favorita stores located in Ecuador. The dataset includes training data with dates, store and product information, promotion details, and sales numbers. Additional files provide supplementary information useful for building predictive models.
Kaggle Competition: https://www.kaggle.com/competitions/store-sales-time-series-forecasting

## File Descriptions and Data Field Information

### `train.csv`
The training data comprises time series of features such as:
- `store_nbr`: Identifies the store at which the products are sold.
- `family`: Identifies the type of product sold.
- `sales`: Gives the total sales for a product family at a particular store on a given date. Fractional values are possible since products can be sold in fractional units (e.g., 1.5 kg of cheese).
- `onpromotion`: Gives the total number of items in a product family that were being promoted at a store on a given date.

### `test.csv`
The test data has the same features as the training data. You will predict the target sales for the dates in this file. The dates in the test data are for the 15 days after the last date in the training data.

### `sample_submission.csv`
A sample submission file in the correct format.

### `stores.csv`
Store metadata, including:
- `city`
- `state`
- `type`
- `cluster`: A grouping of similar stores.

### `oil.csv`
Daily oil price. Includes values during both the train and test data timeframes. Ecuador's economy is highly vulnerable to oil price shocks.

### `holidays_events.csv`
Holidays and events, with metadata. Pay special attention to the `transferred` column:
- A holiday that is transferred officially falls on that calendar day but was moved to another date by the government.
- To find the day it was actually celebrated, look for the corresponding row where `type` is Transfer.
- Days that are `type` Bridge are extra days added to a holiday (e.g., to extend a break across a long weekend). These are frequently made up by the `type` Work Day, which is a day not normally scheduled for work (e.g., Saturday) that is meant to pay back the Bridge.
- `Additional` holidays are days added to a regular calendar holiday, such as typically happens around Christmas (making Christmas Eve a holiday).

- `notebook.ipynb`: This is the main Jupyter notebook where all the data processing, model training, and predictions are done.

- `results/rf_results.csv`: This is the Random Forest model results

### Additional Notes
- Wages in the public sector are paid every two weeks on the 15th and on the last day of the month. Supermarket sales could be affected by this.
- A magnitude 7.8 earthquake struck Ecuador on April 16, 2016. Relief efforts, including donations of water and other first-need products, greatly affected supermarket sales for several weeks after the earthquake.

## License
This project is licensed under the MIT License.

## Files

## How to Run

1. Clone this repository to your local machine.
2. Install the necessary libraries and dependencies using the command `pip install -r requirements.txt`.
3. Open the `notebook.ipynb` file in Jupyter Notebook.
4. Run all the cells in the notebook.