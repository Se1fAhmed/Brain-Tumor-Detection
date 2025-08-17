🧠 Brain Tumor Detection using Swin Transformer

This project is a web-based brain tumor detection system that uses Swin Transformer (a state-of-the-art deep learning model) to classify MRI brain scans into multiple categories. It provides doctors and medical professionals with an easy-to-use interface for uploading MRI images, getting predictions, and generating downloadable PDF reports.

✨ Features

🔐 User Authentication – Register/Login with role-based access (doctor/admin)

📤 MRI Image Upload – Upload MRI scans in PNG/JPG/JPEG/WebP format

🤖 Tumor Classification – Detect tumor types (Glioma, Meningioma, Schwannoma, Neurocytoma, etc.) using Swin Transformer

📊 Prediction Reports – Generate and download detailed PDF reports

🗄️ Database Integration – SQLite (neurosight.db) for storing users & reports

🌐 Web Application – Built with Flask for a lightweight and user-friendly interface

🛠️ Tech Stack

Backend: Flask (Python)

Frontend: HTML, CSS, Bootstrap (via Flask templates)

Deep Learning Model: PyTorch (Swin Transformer)

Database: SQLite (neurosight.db)

Report Generator: WeasyPrint (PDF reports)

📂 Project Structure
BrainTumorDetection/
│── app.py                # Main Flask application

│── models.py             # Database models (User, Reports)

│── static/               # Static files (CSS, JS, images)

│── templates/            # HTML templates

│── neurosight.db         # SQLite database

│── swin_transformer_best_T1.pth  # Pretrained Swin model (T1)

│── swin_transformer_best_T2.pth  # Pretrained Swin model (T2)

│── requirements.txt      # Python dependencies

│── README.md             # Project documentation

⚙️ Installation & Setup
1️⃣ Clone the Repository
cd BrainTumorDetection

2️⃣ Create a Virtual Environment
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows

3️⃣ Install Dependencies
pip install -r requirements.txt

4️⃣ Initialize Database
python
>>> from models import db
>>> from app import app
>>> with app.app_context():
...     db.create_all()

5️⃣ Run the Application
python app.py


Open browser → http://127.0.0.1:5000

🔮 Future Work

Improve UI/UX with modern frontend frameworks

Support DICOM medical imaging format

Deploy on cloud (AWS/GCP/Heroku)

Add explainability (Grad-CAM heatmaps for MRI images)

📚 References

Liu, Ze, et al. Swin Transformer: Hierarchical Vision Transformer using Shifted Windows. arXiv:2103.14030 (2021).

PyTorch Documentation – https://pytorch.org/

Flask Documentation – https://flask.palletsprojects.com/
