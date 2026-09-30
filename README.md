# 🪖 Automated Helmet Violation Detection and Number Plate Recognition Using YOLOv8 and OCR

An AI-based computer vision project for detecting helmet violations among two-wheeler riders and recognizing vehicle number plates using **YOLOv8** and **EasyOCR**.

The project takes road images as input, detects riders and helmet violations, identifies license plates for riders without helmets, extracts license plate text using OCR, and stores the detection results.

---

## 📌 Project Overview

Helmet violations are an important road-safety concern. Manual monitoring of traffic images can be time-consuming and difficult to scale.

This project uses **YOLOv8 object detection** and **EasyOCR** to automate helmet violation detection and number plate recognition.

The system can:

* Detect two-wheelers and riders.
* Detect riders wearing helmets.
* Detect riders without helmets.
* Detect license plates.
* Extract license plate numbers using EasyOCR.
* Count total riders and helmet violations.
* Store the detection results in an Excel file.

---

## 🚀 Key Features

* 🏍️ Two-wheeler detection
* 👤 Rider detection
* 🪖 Helmet detection
* ⚠️ No-helmet violation detection
* 🔍 License plate detection
* 🔤 License plate text recognition using EasyOCR
* 📊 Rider and violation counting
* 📄 Excel-based result storage
* 🖼️ Image-based detection
* 🤖 YOLOv8 deep-learning model

---

## 🧠 System Workflow

```text
Input Road Image
       │
       ▼
    YOLOv8
       │
       ├── Two-Wheeler
       ├── Rider
       ├── Helmet
       ├── No-Helmet
       └── License Plate
                 │
                 ▼
          No-Helmet Rider
                 │
                 ▼
        License Plate Region
                 │
                 ▼
              EasyOCR
                 │
                 ▼
       Extracted Plate Number
                 │
                 ▼
          Detection Results
```

---

## 🛠️ Technologies Used

| Technology       | Purpose                            |
| ---------------- | ---------------------------------- |
| Python           | Programming language               |
| YOLOv8           | Object detection                   |
| OpenCV           | Image processing                   |
| EasyOCR          | License plate text recognition     |
| Pandas           | Data processing                    |
| NumPy            | Numerical operations               |
| Google Colab     | Model training and experimentation |
| Jupyter Notebook | Implementation                     |
| Excel            | Result storage                     |

---

## 🎯 Detection Classes

The YOLOv8 model is trained to detect the following classes:

```text
two-wheeler
rider
helmet
no-helmet
license-plate
```

---

## 📂 Dataset

A custom annotated dataset was used for training the YOLOv8 object detection model.

The dataset was accessed during development through Google Drive in Google Colab:

```text
/content/gdrive/MyDrive/Helmet-Detection.v1i.yolov8
```

The dataset contains annotated images for the required object classes.

> The complete dataset is not included in this repository.

---

## 🏋️ Model Training

The object detection model was trained using **YOLOv8** in Google Colab.

### Training Configuration

```text
Model       : YOLOv8
Image Size  : 640 × 640
Epochs      : 50
Task        : Object Detection
Platform    : Google Colab
```

The training and evaluation process is documented inside the Jupyter Notebook.

---

## 📓 Jupyter Notebook

The complete implementation is available in the notebook:

```text
Helmet_Violation_Detection.ipynb
```

The notebook contains the project workflow, including:

1. Installing required libraries
2. Importing dependencies
3. Connecting Google Drive
4. Loading the dataset
5. Preparing the YOLOv8 configuration
6. Training the detection model
7. Validating the model
8. Running predictions on images
9. Detecting helmet violations
10. Detecting license plates
11. Extracting plate text using EasyOCR
12. Generating detection results

---

## ▶️ How to Run

### Option 1 — Google Colab

The recommended way to run the project is using Google Colab.

1. Open the `.ipynb` notebook.
2. Upload/open it in Google Colab.
3. Connect your Google Drive.
4. Make sure the dataset path matches the path used in the notebook.
5. Run the notebook cells sequentially.
6. Train or load the YOLOv8 model.
7. Provide an input image.
8. Run the detection cells.
9. View the annotated output and extracted license plate information.

### Required Packages

The notebook uses libraries such as:

```text
ultralytics
opencv-python
easyocr
pandas
numpy
openpyxl
```

These can be installed in Colab using:

```python
!pip install ultralytics easyocr opencv-python pandas numpy openpyxl
```

---

## 🖼️ Input and Output

### Input

The system accepts road/traffic images containing two-wheelers and riders.

### Output

The model generates an annotated image showing detected objects such as:

```text
Rider
Helmet
No-Helmet
Two-Wheeler
License Plate
```

For riders detected without helmets, the system attempts to:

```text
Detect License Plate
        ↓
Crop Plate Region
        ↓
Process Image
        ↓
EasyOCR
        ↓
Extract Registration Number
```

The detected information can also be stored in an Excel file.

---

## 📊 Example Result

For an input image containing multiple riders, the system can produce information such as:

```text
Total Riders       : 3
Helmet Riders      : 2
No-Helmet Riders   : 1
License Plate      : Detected
OCR Text            : Vehicle Registration Number
```

*Actual results depend on the input image and model performance.*

---

## 📁 Repository Structure

```text
Helmet-Violation-Detection/
│
├── Helmet_Violation_Detection.ipynb
├── README.md
└── ...
```

Additional model/output files can be added depending on the repository version.

---

## 🔮 Future Enhancements

* Real-time video-based helmet detection
* CCTV camera integration
* Improved license plate recognition
* Vehicle/rider tracking
* Web-based monitoring dashboard
* Database integration
* Automated violation report generation
* Cloud deployment
* Improved OCR for low-quality and angled plates

---

## ⚠️ Limitations

The current implementation is primarily focused on **image-based detection**.

Detection and OCR performance can be affected by:

* Low-resolution images
* Poor lighting
* Occluded license plates
* Small license plates
* Motion blur
* Unusual camera angles
* Overlapping riders or vehicles

License plate OCR accuracy depends heavily on the quality and visibility of the detected plate.

---

## 👩‍💻 Authors

**Y. Lakshmi**
B.Tech – Computer Science Engineering

**B. Uma Maheswari**

**Guide:** G. Balu Narasimha Rao

---

## 🎓 Project Information

**Project Type:** Final Year B.Tech Project
**Domain:** Computer Vision / Deep Learning
**Application:** Road Safety and Automated Traffic Monitoring

---

## 📜 License

This project is intended for academic and educational purposes.
