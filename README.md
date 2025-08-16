❤️A systematic review of predicting elections based on social media data❤️

-> Project Overview
A Flask-based web application for analyzing political news content.  
Users can register, log in, upload datasets, and submit political news for **sentiment classification** (Positive, Negative, Neutral).  
The app uses **TF-IDF + PassiveAggressiveClassifier** for text classification and stores results in **MySQL**.  
It also provides **visualizations** (charts & pie graphs) for insights.

-> Tech Stack
- **Backend:** Flask (Python)
- **Database:** MySQL
- **Machine Learning:** Scikit-learn (TF-IDF, PassiveAggressiveClassifier)
- **Frontend:** HTML, CSS, Jinja2 Templates
- **Libraries:** Pandas, NumPy, Pickle



-> Project Structure

├── app.py # Main Flask application
├── vote.pickle # Trained ML model
├── tfid.pickle # TF-IDF Vectorizer
├── templates/ # HTML Templates (login, register, dashboard, charts, etc.)
├── static/ # Static files (CSS, JS, images)
└── requirements.txt # Python dependencies


-> Getting Started

1. Clone the repository

```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo

2️. Create a virtual environment & install dependencies

bash

python -m venv venv
source venv/bin/activate   # On Linux/Mac
venv\Scripts\activate      # On Windows

pip install -r requirements.txt

3️. Configure MySQL

Create a database named vote
Update MySQL config in app.py if needed:

python

app.config['MYSQL_HOST'] = 'localhost'
app.config['MYSQL_USER'] = 'root'
app.config['MYSQL_PASSWORD'] = 'root'
app.config['MYSQL_DB'] = 'vote'

Create the required tables:

sql

CREATE TABLE people (
  Id INT AUTO_INCREMENT PRIMARY KEY,
  username VARCHAR(100) NOT NULL,
  email VARCHAR(100) NOT NULL,
  password VARCHAR(100) NOT NULL
);

CREATE TABLE review (
  id INT AUTO_INCREMENT PRIMARY KEY,
  news_content TEXT,
  pred VARCHAR(50),
  userid INT,
  parties_name VARCHAR(100),
  FOREIGN KEY (userid) REFERENCES people(Id)
);

4️. Run the Flask App

bash

python app.py
Open http://127.0.0.1:5000/ in your browser.

-> Features

 User Registration & Login
 1. Upload & preview dataset
 2. Submit political news for analysis
 3. ML-powered classification (Positive / Negative / Neutral)
 4. Save results in MySQL
 5. Admin & User dashboards
 6. Data visualization with charts


👨‍💻 Author
Pallavi U Y
📧 pallaviuy11@gmail.com
🔗 linkedin.com/in/pallavi-u-y-383025229
