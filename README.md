# 🩸 AnemiaAI  
### AI-Powered Anemia Detection & Doctor Verification System

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.11-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/SQLAlchemy-red?style=for-the-badge" />
  <img src="https://img.shields.io/badge/SQLite-lightgrey?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Status-Active-success?style=for-the-badge" />
</p>

---

## 🚀 Overview

**AnemiaAI** is a full-stack medical web application built with **FastAPI** that:

- 🧠 Detects anemia type from blood test values  
- 📊 Calculates anemia risk percentage  
- 👤 Allows patients to submit blood analyses  
- 🩺 Allows doctors to confirm or correct AI diagnosis  
- 📈 Displays statistical charts for doctors  
- 💾 Stores full medical history  

> ⚠️ Educational project. Not intended for real clinical use.

---

# ✨ Features

## 👤 Patient Panel

- Registration & Login
- Submit blood parameters
- AI classification:
  - Microcytic anemia
  - Macrocytic anemia
  - Normocytic anemia
  - Normal
- Risk percentage calculation
- View history
- View doctor confirmation or correction

---

## 🩺 Doctor Panel

- View all patient analyses
- See AI preliminary diagnosis
- Approve with recommendations
- Reject with corrected diagnosis
- Status tracking:
  - `Pending`
  - `Confirmed`
  - `Rejected`
- 📊 Blood statistics chart (Chart.js)

---

# 🧠 AI Logic

### Classification Rules

| Condition | Result |
|-----------|--------|
| HB ≥ 120 | Normal |
| HB < 120 & MCV < 80 | Microcytic anemia |
| HB < 120 & MCV > 100 | Macrocytic anemia |
| HB < 120 & 80 ≤ MCV ≤ 100 | Normocytic anemia |

### Risk Formula

```python
risk = ((120 - hb) / 120) * 100
```



# 🏗 Project Structure

anemia_ai_project/
│
├── app/
│ ├── main.py
│ ├── models.py
│
├── templates/
│ ├── base.html
│ ├── home.html
│ ├── dashboard.html
│ ├── doctor_dashboard.html
│ ├── login.html
│ ├── register.html
│ ├── about.html
│ ├── types.html
│ ├── contacts.html
│
├── static/
│ ├── style.css
│ ├── app.js
│
├── anemia.db
├── requirements.txt
└── README.md


---

# ⚙️ Installation Guide

## 1️⃣ Clone Repository
```
git clone https://github.com/your-username/anemia-ai.git
cd anemia-ai
```

---

## 2️⃣ Create Virtual Environment

### Windows
```
python -m venv venv
venv\Scripts\activate
```

### Mac / Linux
```
python3 -m venv venv
source venv/bin/activate
```

---

## 3️⃣ Install Dependencies
```
pip install fastapi uvicorn sqlalchemy jinja2 python-multipart
```

Or using requirements file:
```
pip install -r requirements.txt
```

---

## 4️⃣ Run Application
```
python -m uvicorn app.main:app --reload
```

---

## 5️⃣ Open in Browser
```
http://127.0.0.1:8000
```

---

# 🗄 Reset Database (If Model Changes)

If you get database errors:
```
del anemia.db
```
Then restart the server.

---

# 🔐 User Roles

| Role | Access |
|------|--------|
| patient | Submit and view own analyses |
| doctor | View all analyses and confirm/reject |

---

# 📊 Doctor Dashboard Analytics

The system automatically calculates average:

- Hemoglobin
- RBC
- MCV
- MCH
- Platelets

Displayed using interactive **Chart.js** bar chart.

---

# 🎨 Frontend Design

- Modern turquoise medical theme
- Vertical clean input forms
- Styled action buttons
- Responsive layout
- Status highlighting

---

# 🛠 Technology Stack

## Backend
- FastAPI
- SQLAlchemy ORM
- SQLite Database
- Jinja2 Templates

## Frontend
- HTML5
- CSS3
- JavaScript
- Chart.js

---

# 🔮 Future Improvements

- Password hashing (bcrypt)
- JWT authentication
- PostgreSQL support
- Docker containerization
- Real Machine Learning model
- Deployment to cloud (Render / Railway / AWS)

---

# 📜 License

MIT License

---

# 👨‍💻 Author

CS-2428 Arnuruly Yestay, Sansyzbay Kaisarbek

---

<p align="center">
⭐ If you like this project, give it a star on GitHub!
</p>
