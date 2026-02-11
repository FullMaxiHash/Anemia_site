🩸 AnemiaAI — AI-Powered Anemia Detection System
<p align="center"> <b>Full-Stack Medical Web Application built with FastAPI</b><br> AI-based anemia type prediction + Doctor verification system </p>
🚀 About The Project

AnemiaAI is a role-based medical web platform that:

Analyzes blood test parameters

Predicts anemia type using AI logic

Calculates anemia risk percentage

Allows doctors to confirm or correct AI diagnosis

Stores full medical history in a database

Displays statistical charts for doctors

This project demonstrates full-stack development skills with backend logic, authentication, database modeling, and frontend visualization.

⚠️ This system is for educational purposes only and does not replace professional medical advice.

✨ Features
👤 Patient

Registration & Login

Submit blood test parameters

Get AI-predicted anemia type

View risk percentage

View history of analyses

See doctor confirmation or correction

🩺 Doctor

View all patient analyses

See AI preliminary diagnosis

Approve diagnosis (add recommendations)

Reject diagnosis (add corrected diagnosis)

View average blood parameter statistics (Chart.js)

Status tracking:

Pending

Confirmed

Rejected

🧠 AI Diagnosis Logic

Anemia type is classified based on Hemoglobin (HB) and MCV:

Condition	Diagnosis
HB ≥ 120	Normal
HB < 120 & MCV < 80	Microcytic anemia
HB < 120 & MCV > 100	Macrocytic anemia
HB < 120 & 80 ≤ MCV ≤ 100	Normocytic anemia

Risk is calculated proportionally based on hemoglobin deficiency.

🏗 Project Structure
anemia_ai_project/
│
├── app/
│   ├── main.py
│   ├── models.py
│
├── templates/
│   ├── base.html
│   ├── home.html
│   ├── dashboard.html
│   ├── doctor_dashboard.html
│   ├── login.html
│   ├── register.html
│   ├── about.html
│   ├── types.html
│   ├── contacts.html
│
├── static/
│   ├── style.css
│   ├── app.js
│
├── anemia.db
├── requirements.txt
└── README.md

🛠 Tech Stack
Backend

FastAPI

SQLAlchemy

SQLite

Jinja2

Frontend

HTML5

CSS3

JavaScript

Chart.js

⚙️ Installation Guide
1️⃣ Clone the repository
git clone https://github.com/your-username/anemia-ai.git
cd anemia-ai

2️⃣ Create virtual environment (recommended)
python -m venv venv


Activate:

Windows

venv\Scripts\activate


Mac/Linux

source venv/bin/activate

3️⃣ Install dependencies
pip install -r requirements.txt


If requirements.txt doesn't exist:

pip install fastapi uvicorn sqlalchemy jinja2 python-multipart

4️⃣ Run the server
python -m uvicorn app.main:app --reload

5️⃣ Open in browser
http://127.0.0.1:8000

🗄 Database Reset

If you changed models and get errors:

Delete database file:

del anemia.db


Then restart server.

🔐 Default Roles

You can create users during registration.

To create doctor manually (example):

In database, role must be:

doctor


For patients:

patient

📊 Doctor Statistics

Doctor dashboard includes:

Bar chart of average:

HB

RBC

MCV

MCH

PLT

All patient analyses

Diagnosis validation system

📌 Future Improvements

Real Machine Learning model

Password hashing (bcrypt)

JWT Authentication

PostgreSQL production database

Docker containerization

API versioning

Dark mode

Admin analytics dashboard

Deployment on Render / Railway

🎓 Educational Purpose

This project demonstrates:

Full-stack web architecture

Role-based authentication

ORM database modeling

Medical AI logic

Frontend data visualization

📜 License

MIT License — free to use for educational and portfolio purposes.

💡 Author

Developed as an AI-powered medical research system.
