# Heart Disease Prediction – Model Deployment (Flask API)

## 📌 Project Overview

This project demonstrates the deployment of a Machine Learning classification model using **Flask**. The trained Logistic Regression model predicts whether a person is likely to have heart disease based on medical input features. The model is exposed as a REST API endpoint and tested using Thunder Client / Postman.

---

## 🧠 Model Details

* **Algorithm:** Logistic Regression
* **Task Type:** Binary Classification
* **Target Variable:** Presence of heart disease (0 = No, 1 = Yes)
* **Model File:** `model.pkl`

The model was trained earlier using the UCI Heart Disease dataset and then saved using `pickle`.

---

## 📁 Project Structure

```
Alfido_Task3_Model_Deployment/
│
├── app.py               # Flask application
├── model.pkl            # Trained ML model
├── requirements.txt     # Required Python libraries
└── README.md            # Project documentation
```

---

## ⚙️ Requirements

Install the required dependencies using:

```bash
pip install -r requirements.txt
```

### Main Libraries Used:

* Flask
* scikit-learn
* numpy
* pandas

---

## ▶️ How to Run the Application

1. Open terminal / command prompt
2. Navigate to the project folder:

```bash
cd Alfido_Task3_Model_Deployment
```

3. Run the Flask app:

```bash
python app.py
```

4. The server will start at:

```
http://127.0.0.1:5000
```

---

## 🔗 API Endpoint Details

### ➤ Predict Endpoint

* **URL:** `/predict`
* **Method:** POST
* **Input Format (JSON):**

```json
{
  "features": [63,145,233,150,2.3,0,1,0,0,1,1,0,0,0,1,0,0,1]
}
```

⚠️ The model expects **18 numerical features** in the correct order.

* **Output Format (JSON):**

```json
{
  "prediction": 1
}
```

---

## 🧪 Testing the API

The API was tested using **Thunder Client** in Visual Studio Code:

* Request sent with JSON body
* Successful response received with status **200 OK**
* Prediction returned correctly

---



## ✅ Conclusion

This task successfully demonstrates how to deploy a Machine Learning model using Flask, expose it via a REST API, and test it locally. It completes the **Model Deployment** requirement for the internship project.


