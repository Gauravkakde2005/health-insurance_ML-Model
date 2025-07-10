# 🏥 Medical Insurance Charges Predictor

A **Machine Learning** web application using **FastAPI** that predicts medical insurance charges based on user inputs like age, sex, BMI, smoking status, number of children, and region.

---

## 🔍 Problem Statement

Insurance companies estimate charges based on several factors. This project uses a **regression model** to predict insurance costs for a person based on medical and demographic information.

---

## 🚀 Tech Stack

- **Frontend:** HTML (Jinja2 Templates)
- **Backend:** FastAPI
- **Model:** scikit-learn (`model.pkl`)
- **Language:** Python
- **Server:** Uvicorn
- **Notebook:** Jupyter (`.ipynb`)
- **Deployment Ready:** ✅

---

## 📂 Project Structure

```
.
├── templates/
│   └── index.html          # Web form UI
├── model.pkl               # Trained ML model
├── main.py                 # FastAPI backend code
├── medical.ipynb           # Jupyter Notebook - model training
├── README.md               # Project documentation
```

---

## 🧠 Model Information

- **Dataset:** Medical Insurance Dataset
- **Algorithm Used:** (e.g., `LinearRegression`, `XGBRegressor`) *(Refer to `medical.ipynb`)*
- **Input Features:**
  - `age` — Age of the individual
  - `sex` — Gender (Male/Female)
  - `bmi` — Body Mass Index
  - `children` — Number of children
  - `smoker` — Smoking habit (Yes/No)
  - `region` — Residential area
- **Target Variable:** `charges` (insurance cost)

---

## ⚙️ How to Run the Project

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/Gauravkakde2005/health-insurance_ML-Model.git
cd health-insurance_ML-Model
```

### 2️⃣ Install Required Packages

```bash
pip install -r requirements.txt
```

> Example `requirements.txt`:
> ```
> fastapi
> uvicorn
> pandas
> numpy
> scikit-learn
> jinja2
> ```

### 3️⃣ (Optional) Train the Model

If `model.pkl` is not available:

- Open `medical.ipynb`
- Train the model
- Save model using:

```python
import pickle
pickle.dump(model, open('model.pkl', 'wb'))
```

### 4️⃣ Start the FastAPI Server

```bash
uvicorn main:app --reload
```

Visit: [http://localhost:8000](http://localhost:8000)

---

## 📮 API Endpoints

| Method | Endpoint   | Description               |
|--------|------------|---------------------------|
| GET    | `/`        | Loads the web UI          |
| POST   | `/predict` | Returns prediction (JSON) |

### ✅ Example Request

```json
{
  "age": 30,
  "sex": "Male",
  "bmi": 28.7,
  "children": 1,
  "smoker": "No",
  "region": "Southwest"
}
```

### 🔁 Example Response

```json
{
  "predicted_charges": 4325.67
}
```

---

## 🖼️ UI Preview

![UI Screenshot](./d5b8d053-b53f-475e-bb22-4ba7cdf321d7.png)

---

## 🔮 Future Improvements

- Deploy on Render/Heroku/Vercel
- Add user authentication
- Improve model with hyperparameter tuning
- Add visual charts to display predictions

---

## 🙋‍♂️ Author

**Gaurav Kakde**  
*Computer Science | AI & Data Science Student*  
GitHub: [@Gauravkakde2005](https://github.com/Gauravkakde2005)

---
