# 🎵 Sound Emotion Detector - How to Run

## Prerequisites
- **Python 3.11** (required for compatibility with numba/llvmlite)
- A web browser (Chrome recommended)

---

## Step 1: Create Virtual Environment

```bash
python3.11 -m venv env
```

## Step 2: Activate Virtual Environment

**macOS / Linux:**
```bash
source env/bin/activate
```

**Windows:**
```bash
env\Scripts\activate
```

## Step 3: Install Dependencies

First install `llvmlite` and `numba` (these need to be installed before librosa):
```bash
pip install llvmlite==0.43.0 numba==0.60.0
```

Then install the remaining packages:
```bash
pip install flask flask-sqlalchemy pymysql librosa soundfile scikit-learn scipy
```

## Step 4: Run the Application

```bash
python app.py
```

You should see output like:
```
 * Serving Flask app 'app'
 * Debug mode: on
 * Running on http://127.0.0.1:5000
```

## Step 5: Open in Browser

Open your browser and go to:

👉 **http://127.0.0.1:5000**

Or run this command to open directly in Chrome:
```bash
open -a "Google Chrome" http://127.0.0.1:5000
```

---

## ⚠️ Notes

- The app uses **SQLite** by default (configured in `config.json`). No external database setup needed.
- Upload `.wav` audio files on the Upload page to detect emotions.
- The pre-trained ML model is stored in `sound_recog.txt`.
- Make sure the `uploads/` folder exists (the app creates it automatically).

---

## Quick Run (All-in-One)

```bash
# From the project root directory:
python3.11 -m venv env
source env/bin/activate
pip install llvmlite==0.43.0 numba==0.60.0
pip install flask flask-sqlalchemy pymysql librosa soundfile scikit-learn scipy
python app.py
```
