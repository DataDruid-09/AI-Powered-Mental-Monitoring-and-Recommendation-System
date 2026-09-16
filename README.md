# 🧠 AI-Powered Mental Health Monitoring & Recommendation System

> **An AI-driven system for text-based emotion detection, mood tracking, and personalized recommendations.**

The **AI-Powered Mental Health Monitoring and Recommendation System** is a machine-learning-based web application designed to analyze a user's daily text input, detect their emotional state, provide emotion-based recommendations, and maintain a history of emotional patterns.

The system combines **Natural Language Processing (NLP), Machine Learning, Flask, SQLite, and external API integration** to create a simple and interactive platform for emotional monitoring.

> ⚠️ **Note:** This project focuses on text-based emotion detection and supportive recommendations. It is not intended for medical diagnosis or clinical assessment.

---

## ✨ Key Features

### 🤖 AI-Based Emotion Detection

* Accepts natural-language text from the user.
* Cleans and preprocesses the input using NLP techniques.
* Converts text into numerical features using **TF-IDF**.
* Uses a trained Machine Learning model to classify emotions.
* Includes a fallback rule-based detection mechanism for reliability.

### 💡 Emotion-Based Recommendations

The system generates recommendations based on the detected emotional state and provides supportive content relevant to the user's mood.

### 🎬 YouTube Recommendations

The project integrates the **YouTube API** to provide video recommendations based on the user's detected mood.

### 📅 Mood History & Calendar

* Stores previous mood-test results.
* Provides a mood calendar for tracking emotional states.
* Allows users to check previous test results.
* Supports monthly emotion analysis.

### 🔐 User Authentication

* User registration
* Login functionality
* Password hashing
* Session management
* User-specific data storage

### 📊 Emotion Visualization

The system generates emotion trend charts to help users understand their emotional patterns over time.

---

## 🧠 How It Works

```text
                  User
                   │
                   ▼
          ┌─────────────────┐
          │   Text Input    │
          └────────┬────────┘
                   │
                   ▼
          ┌─────────────────┐
          │ NLP Preprocess  │
          └────────┬────────┘
                   │
                   ▼
          ┌─────────────────┐
          │     TF-IDF      │
          │ Feature Extract │
          └────────┬────────┘
                   │
                   ▼
          ┌─────────────────┐
          │  ML Prediction  │
          └────────┬────────┘
                   │
             Detected Mood
                   │
          ┌────────┴─────────┐
          ▼                  ▼
 ┌─────────────────┐  ┌─────────────────┐
 │ Recommendations │  │ YouTube Videos  │
 └─────────────────┘  └─────────────────┘
          │
          ▼
 ┌────────────────────┐
 │  Mood History DB   │
 └─────────┬──────────┘
           │
           ▼
 ┌────────────────────┐
 │ Mood Calendar &    │
 │ Emotion Analytics  │
 └────────────────────┘
```

The system follows a pipeline of **user input → NLP preprocessing → TF-IDF feature extraction → emotion prediction → recommendations → mood history and visualization**.

---

## 🛠️ Technology Stack

| Technology          | Usage                                  |
| ------------------- | -------------------------------------- |
| 🐍 **Python**       | Core development and ML implementation |
| 🌐 **Flask**        | Backend web framework                  |
| 🧠 **Scikit-learn** | Machine Learning and TF-IDF            |
| 📝 **NLTK**         | Natural Language Processing            |
| 🐼 **Pandas**       | Dataset processing                     |
| 🔢 **NumPy**        | Numerical operations                   |
| 🗄️ **SQLite**      | User and mood-history database         |
| 🎨 **HTML/CSS**     | Frontend interface                     |
| 🎬 **YouTube API**  | Mood-based video recommendations       |
| 💻 **VS Code**      | Development environment                |

The project's documented software requirements include Python, NLTK, Scikit-learn, Pandas, NumPy, Flask, HTML/CSS, and SQLite.

---

## 🔄 Project Workflow

```text
1. User Registration / Login
              ↓
2. User Enters Daily Feelings
              ↓
3. Text Cleaning & Preprocessing
              ↓
4. TF-IDF Feature Extraction
              ↓
5. Machine Learning Prediction
              ↓
6. Emotion Classification
              ↓
7. Generate Personalized Suggestions
              ↓
8. Recommend Mood-Based Videos
              ↓
9. Store Result in SQLite
              ↓
10. Display Mood History & Charts
```

---

## 🧩 System Modules

### 1. Frontend

Collects user input and displays predictions, recommendations, charts, and other application outputs.

### 2. Backend

Handles application logic, routing, data processing, model communication, and database interaction.

### 3. AI Model & Recommendation Engine

Processes user text, predicts emotions, and generates suggestions based on the detected emotional state.

### 4. Database

Stores user information, input data, predictions, and recommendations.

### 5. Visualization

Displays emotion charts and mood-tracking information for analyzing emotional patterns.

---

## 🔐 Authentication & Data Management

The application uses **SQLite** to manage user and mood-history data.

The authentication workflow includes:

```text
Register
   ↓
Password Hashing
   ↓
User Stored in Database
   ↓
Login
   ↓
Session Management
   ↓
Access Personalized Data
```

The implementation includes separate user and mood-history tables, along with password hashing and session management.

---

## 📊 Application Screens

The application includes the following primary interfaces:

* 🏠 **Home Page**
* 🔐 **Login Page**
* 📝 **Registration Page**
* 📊 **Dashboard**
* 🧪 **Emotion Test Interface**
* 😊 **Mood Prediction Result**
* 💡 **Recommendation Section**
* 📅 **Mood Calendar**

The frontend was implemented using HTML templates connected with Flask routes and backend functionality.

---

## 🧪 Machine Learning Pipeline

The Machine Learning implementation consists of:

### Text Preprocessing

* Text cleaning
* Removal of unwanted words and characters
* Conversion of textual data into numerical representation

### Feature Extraction

**TF-IDF (Term Frequency–Inverse Document Frequency)** is used to transform textual data into numerical features suitable for Machine Learning.

### Model Training

```text
Dataset
   ↓
Text Preprocessing
   ↓
TF-IDF
   ↓
Train / Test Split
   ↓
Model Training
   ↓
Testing
   ↓
Emotion Prediction
```

The project explored suitable algorithms for emotion detection and trained the selected model using the preprocessed dataset.

---

## 📅 Development Approach

The project was developed using the **Agile Software Development Life Cycle**, with implementation divided into iterative development sprints.

Major development phases included:

```text
Week 1 → Environment & Project Setup
Week 2 → Dataset & NLP Preprocessing
Week 3 → ML Model Development
Week 4 → Flask Backend
Week 5 → Database & Authentication
Week 6 → Frontend Development
Week 7 → ML Model Integration
Week 8 → Recommendations & Mood Tracking
```

This iterative approach allowed the system to be tested and improved throughout development.

---

## 📁 Suggested Repository Structure

```text
AI-Mental-Health-Monitoring/
│
├── backend/
│   ├── app.py
│   ├── config.py
│   └── ...
│
├── templates/
│   ├── home.html
│   ├── login.html
│   ├── register.html
│   └── dashboard.html
│
├── static/
│   ├── css/
│   └── js/
│
├── model/
│   ├── emotion_model.pkl
│   └── vectorizer.pkl
│
├── dataset/
│   └── ...
│
├── database/
│   └── mental_health.db
│
├── notebooks/
│   └── emotion_training.ipynb
│
├── requirements.txt
├── .gitignore
└── README.md
```

*Adjust the folder names above to match your actual GitHub repository structure.*

---

## 🚀 Project Highlights

* 🧠 NLP-based text emotion detection
* 📊 TF-IDF feature extraction
* 🤖 Machine Learning-based emotion classification
* 🌐 Flask web application
* 🔐 User authentication with password hashing
* 🗄️ SQLite database integration
* 📅 Mood calendar and history tracking
* 📈 Emotion trend visualization
* 💡 Emotion-based recommendations
* 🎬 YouTube API integration
* 🛡️ Handling of empty and invalid inputs
* 🔄 Agile-based iterative development

---

## 🔮 Future Scope

The current system is focused specifically on **text-based emotion detection** and does not cover voice-based analysis or medical diagnosis.

Possible future enhancements include:

* 🎙️ Voice-based emotion detection
* 📷 Facial emotion recognition
* 🧠 Advanced NLP / Transformer models
* 📱 Mobile application
* 📈 More advanced mood analytics
* 🌍 Multilingual emotion detection
* 🔔 Personalized mood notifications
* ☁️ Cloud deployment
* 🔐 Enhanced data security and privacy mechanisms

---

## 🎓 Academic Project

**Project Title:** AI-Powered Mental Health Monitoring and Recommendation System

**Institution:** Pune District Education Association's College of Engineering, Manjari, Pune

**Department:** Computer Engineering

**Project Guide:** Prof. A. A. Bamanikar

### 👥 Team

| Member               | Role                           |
| -------------------- | ------------------------------ |
| **Shubham Kamble**   | Project Development / ML       |
| **Shlok Ekhande**    | Frontend Development           |
| **Sagar Ingole**     | Documentation & Testing        |
| **Roshan Jayabhaye** | Backend & Database Integration |

---

## 📌 Disclaimer

This project is developed for **academic and educational purposes**. The system performs text-based emotion classification and provides general recommendations based on detected emotions. It is **not a medical diagnostic tool** and should not be considered a replacement for qualified mental-health professionals.

---

## ⭐ Project

If you find this project useful or interesting, feel free to **star ⭐ the repository** and explore the implementation.
