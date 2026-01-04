CliniScan: AI-Powered Lung Abnormality Detection

CliniScan is a deep learning-based object detection system designed to identify and localize 17 different types of lung abnormalities from Chest X-ray images. Built using YOLOv8 and deployed via Streamlit, this project is optimized for high-speed training and inference on NVIDIA GPUs (RTX 4050).

🚀 Features

High-Speed Training: Optimized pipeline using YOLOv8 Nano for rapid iteration.

GPU Accelerated: Leverages CUDA for both training and real-time inference.

Interactive UI: Streamlit-based web application for easy X-ray uploads and results visualization.

Pathology Detection: Detects 17 findings including Cardiomegaly, Pleural Effusion, Atelectasis, and more.

🛠️ Tech Stack

Model: Ultralytics YOLOv8

UI: Streamlit

Data Handling: Pandas, NumPy

Deep Learning: PyTorch (with CUDA support)

📁 Project Structure

CliniScan-Project/
├── data/
│   ├── raw/                # Original images and data.csv (Excluded from Git)
│   └── processed/          # YOLO formatted labels (Excluded from Git)
├── src/
│   ├── 1_preprocess_annotations.py 
│   ├── 2_split_data.py             
│   ├── 4_train_yolo.py             
│   └── streamlit_app.py    # Web Application
├── weights/                # Trained model weights (best.pt)
└── requirements.txt


⚙️ Setup & Installation

Clone the Repository:

git clone [https://github.com/YOUR_USERNAME/CliniScan-Lung-Abnormality-Detection.git](https://github.com/YOUR_USERNAME/CliniScan-Lung-Abnormality-Detection.git)
cd CliniScan-Lung-Abnormality-Detection


Setup Virtual Environment:

python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate


Install Dependencies:

pip install -r requirements.txt


Run the App:

streamlit run src/streamlit_app.py


📊 Dataset

This project utilizes the VinBigData Chest X-ray Dataset. Due to the size of the images and the CSV annotations, the raw data is not included in this repository.

Disclaimer: This tool is for educational/research purposes only and is not a substitute for professional medical diagnosis.
