# Energy Consumption Prediction using Machine Learning (LSTM)

## 📌 Abstract
This project focuses on predicting electricity consumption using data from Finland's transmission system operator. The goal was to evaluate whether a machine learning model could provide accurate results in a complex forecasting task, while also exploring advanced predictive techniques.  
We used a **Long Short-Term Memory (LSTM)** model to forecast energy demand based on six years of hourly electricity consumption data, which forms a seasonal univariate time series.  
The model's performance was assessed using **Root Mean Squared Error (RMSE)** for direct comparability with real energy readings.  
The results show that machine learning can effectively forecast electricity usage, enabling:
- Better deployment of renewable energy sources  
- Improved planning for high and low load days  
- Reduced wastage from maintaining polluting standby generation  

---

## 📊 Dataset
- **Source:** Finland's Transmission System Operator  
- **Format:** CSV file  
- **Total Observations:** 52,965  
- **Variables:** 5  
- **Load Volume Stats:**
  - Minimum: 5,341 MWh  
  - Maximum: 15,105 MWh  
  - Average: 9,488.75 MWh  

The dataset is a **univariate time series**, with one column representing time and another representing energy consumption.

---

## 🔄 Data Preprocessing
1. **Down-sampling:**  
   - Converted from hourly frequency to daily frequency using Pandas `resample()` function.  
   - This reduced the granularity of the data for day-level predictions.  
2. **Training/Validation Split:**  
   - Data was split into training and validation sets for model evaluation.  

---

## 🤖 Model Implementation
- **Algorithm:** Long Short-Term Memory (LSTM) Neural Network  
- **Epochs:** 60 (entire dataset passed through the model 60 times)  
- **Batch Size:** 20 (model weights updated after every 20 samples)  
- **Evaluation Metric:** RMSE  

The LSTM model was trained on historical daily consumption data and validated on unseen data to assess its predictive capability.

---

## 📈 Results
- The LSTM model successfully predicted electricity demand trends with promising accuracy.
- Forecasts can assist in:
  - Renewable energy integration
  - Peak/off-peak load planning
  - Minimizing energy wastage from standby generation

---

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/paritosh6750/Energy-Consumption-Prediction-Using-LSTM.git
