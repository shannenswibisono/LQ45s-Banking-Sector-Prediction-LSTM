# Predicting Closing Prices of Banking Stocks in LQ45 Using LSTM

Recent studies suggest that LSTM networks are good at predicting stock prices, especially for longer timeframes. 

## Data: 
I used LSTM to predict the closing prices of six banking stocks in the LQ45 index (August 2023 to January 2024). I collected daily data for BBCA, BBNI, BBRI, BMRI, BBTN, and BRIS from March 11, 2019, to March 11, 2024. I cleaned the data by removing null values and days with zero trading volume. Then, I divided the data into 90% for training and 10% for testing.

## LSTM Setup:
I designed a three-layer LSTM network with 50 neurons in the LSTM layer, followed by a dense layer and a dropout layer. Dropout helps prevent overfitting by randomly ignoring 20% of the information during processing. To train the model, I used mean square error (MSE) as the loss function and the Adam optimizer. The LSTM layer uses the tanh activation function to capture complex patterns. The model was trained for 50 epochs, with each epoch consisting of batches of 32 data points. I monitored the training process using the loss metric, continuing training until the improvement stabilized (with minimum delta = 0.0001).

## Results:
After running the model 50 times and averaging the results for each day to ensure consistency, I obtained the RMSE and MAPE for the six stocks:
# BCA
<img width="979" alt="Screen Shot 2024-05-12 at 23 50 49" src="https://github.com/shannenswibisono/LQ45s-Banking-Sector-Prediction-LSTM/assets/155773383/163a9ac9-2cd0-4ee2-9339-ddfa80027629">

# BRI
<img width="992" alt="Screen Shot 2024-05-12 at 23 52 11" src="https://github.com/shannenswibisono/LQ45s-Banking-Sector-Prediction-LSTM/assets/155773383/a20c60a6-3d40-44a1-b26d-a81e3564babb">

# BNI
![Screen Shot 2024-05-12 at 23 52 41](https://github.com/shannenswibisono/LQ45s-Banking-Sector-Prediction-LSTM/assets/155773383/fc74ccfd-0ff9-41f4-ab58-cba391c4e173)

# Mandiri
<img width="983" alt="Screen Shot 2024-05-12 at 23 53 42" src="https://github.com/shannenswibisono/LQ45s-Banking-Sector-Prediction-LSTM/assets/155773383/82500f48-379d-4bec-9cbf-b38b22be2ff3">

# BTN
<img width="984" alt="Screen Shot 2024-05-12 at 23 54 46" src="https://github.com/shannenswibisono/LQ45s-Banking-Sector-Prediction-LSTM/assets/155773383/ea9878b3-68f5-4a6d-b1da-9aba16920ae7">

# BRIS
<img width="976" alt="Screen Shot 2024-05-12 at 23 55 19" src="https://github.com/shannenswibisono/LQ45s-Banking-Sector-Prediction-LSTM/assets/155773383/ebdec7b3-fde4-416e-bca0-8d59c2c1dd8d">
