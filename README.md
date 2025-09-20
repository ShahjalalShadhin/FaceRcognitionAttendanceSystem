# Face Recognition Attendance System

## 📌 Overview

This project is a **Face Recognition-based Attendance System** built with Python and OpenCV.
It uses a **webcam** to detect and recognize faces, compares them with stored images, and marks attendance in **real-time** using **Firebase**.

* ✅ Detects and recognizes faces using `dlib` & `face-recognition` library
* ✅ Matches detected face with database images
* ✅ Marks attendance once per person according to time mentioned in code
* ✅ Saves & updates attendance in **Firebase Firestore**
* ✅ Simple interface with background and mode images

## 📂 Project Structure

```
FaceRecognitionRealTime/
│── .venv/                     # Virtual environment  
│── Images/                    # Database images of subjects  
│── Resources/  
│   ├── Modes/                 # Interface images for webcam attendance UI  
│   └── background.png         # Background interface image  
│── .gitignore                 # Git ignore file  
│── AddDataToDatabase.py       # Script to add data to Firebase  
│── EncodeGenerator.py         # Encodes images & stores for recognition  
│── facerecognition.py         # Main file to run system (webcam + recognition + attendance)  
│── EncodeFile.p               # Stored encodings of face images  
│── requirements.txt           # Python dependencies  
│── serviceAccountKey.json     # Firebase service key (❌ should not be pushed to GitHub)  
```

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/YourUsername/FaceRecognitionAttendanceSystem.git
cd FaceRecognitionAttendanceSystem
```

### 2. Create Virtual Environment & Activate

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# Linux / Mac
source .venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

## 🚀 Usage

### 1. Add Images

* Place images of subjects inside the `Images/` folder.
* File name should match **student name or ID**.

### 2. Generate Encodings

```bash
python EncodeGenerator.py
```

### 3. Run Attendance System

```bash
python facerecognition.py
```

📷 The webcam will open:

* Detects faces in real-time
* Matches with database
* Updates attendance in **Firebase**
* If attendance already marked within time mentioned → shows **"Already Marked"**

## 🔥 Firebase Setup

1. Create a Firebase project in [Firebase Console](https://console.firebase.google.com/).
2. Enable **Firestore Database** & **Storage**.
3. Download `serviceAccountKey.json` and place it in the project root (⚠️ add it to `.gitignore`).
4. Update Firebase configuration in the scripts.

## 🛠️ Technologies Used

* Python
* OpenCV
* Dlib & face-recognition
* Firebase (Firestore & Storage)

## 📌 Features

* Real-time face detection & recognition
* Attendance saved in Firebase
* Prevents duplicate marking (valid for the time mentioned in the code)
* Extensible with more subjects

## ⚠️ Note

* Do **not** push `serviceAccountKey.json` to GitHub.
* Use `.gitignore` to exclude sensitive files.


## 👨‍💻 Author

**Md. Shahjalal Shadhin**
