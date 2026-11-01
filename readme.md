# 🧠 CerebroVision V3 – Intelligent Neuro-Oncology MRI Analysis

<p align="center">
  <b>Exploring the power of AI in brain MRI analysis.</b>
</p>

CerebroVision V3 is an AI-powered brain MRI analysis project that combines machine learning and deep learning to detect brain tumors and classify their types. The project aims to explore how artificial intelligence can make medical image analysis more accessible, interactive, and efficient.

Using a hybrid deep learning and machine learning approach, CerebroVision extracts meaningful features from MRI images and uses trained classifiers to generate predictions through an interactive web application.

## ✨ Key Features

- **Brain Tumor Detection:** Identifies whether an MRI image indicates a tumor or a healthy scan.
- **Tumor Classification:** Classifies supported tumor types:
  - Glioma
  - Meningioma
  - Pituitary
- **AI-Based Analysis:** Uses ResNet-50 for feature extraction and PCA with SVM for classification.
- **Interactive Dashboard:** Upload MRI images and view prediction results.
- **Prediction History:** Maintains a record of previous analyses.
- **Performance Monitoring:** Displays model-related statistics through the dashboard.

## ⚙️ How It Works

CerebroVision follows a two-stage analysis pipeline:

1. **MRI Image Input:** The user uploads a brain MRI image.
2. **Preprocessing:** The image is prepared for feature extraction.
3. **Feature Extraction:** A pretrained ResNet-50 model extracts 2048-dimensional features.
4. **Dimensionality Reduction:** PCA reduces the feature dimensions.
5. **Classification:** The trained SVM classifier generates the prediction.
6. **Result Display:** The frontend displays the prediction and stores analysis history.

## 🏗️ Project Architecture

```text
CerebroVision-V3/
│
├── backend/          # FastAPI backend and prediction APIs
├── frontend/         # React-based user interface
├── classifiers/      # Machine learning classifiers
├── dataset/          # MRI dataset files
├── evaluation/       # Model evaluation scripts
├── features/         # Extracted feature files
├── models/           # Trained models and preprocessing objects
├── notebooks/        # Experiments and analysis
├── preprocessing/    # MRI preprocessing utilities
└── README.md
```

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core development |
| PyTorch | ResNet-50 feature extraction |
| Scikit-learn | PCA and machine learning |
| OpenCV | Image preprocessing |
| FastAPI | Backend and REST APIs |
| React | Frontend development |
| Vite | Frontend development server |
| SQLite | Prediction history and storage |
| NumPy | Numerical computations |
| Joblib | Saving and loading trained models |

## 🚀 Getting Started

### Prerequisites

- Python 3.11
- Node.js and npm
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/JayIngale24/https://github.com/JayIngale24/CerebroVision.git
```

### 2. Navigate to the Project

```bash
cd CerebroVision-V3
```

### 3. Set Up the Backend

Create and activate a virtual environment:

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
```

Install dependencies:

```bash
pip install -r backend/requirements.txt
```

Start the backend from the project root:

```bash
python -m uvicorn backend.main:app --host 127.0.0.1 --port 8000
```

Backend API:

`http://127.0.0.1:8000`

### 4. Set Up the Frontend

Open another terminal:

```bash
cd frontend
npm install
npm run dev
```

Open the local URL displayed by Vite in your browser.

## 📊 Machine Learning Approach

CerebroVision uses a hybrid approach:

- **ResNet-50:** Extracts deep features from MRI images.
- **PCA:** Reduces feature dimensions.
- **SVM:** Performs classification using the extracted features.
- **Random Forest:** Also available as an alternative classifier for experimentation.

The system uses a two-stage approach: tumor detection with the BR35H dataset and tumor-type classification with the Cheng/T1-CE dataset.

## 🔬 Future Improvements

- Compare SVM, Random Forest, XGBoost, and CNN models.
- Perform comprehensive model evaluation.
- Add explainable AI techniques for better model interpretability.
- Improve MRI preprocessing and validation.
- Enhance dashboard reporting and visualization.
- Strengthen input validation and prediction reliability.

## ⚠️ Disclaimer

CerebroVision V3 is an educational and research prototype. It is not a certified medical device and should not be used as a substitute for professional medical advice, radiological interpretation, or clinical diagnosis.

## 👨‍💻 Project

**CerebroVision V3 – Intelligent Neuro-Oncology MRI Analysis**

Developed as an exploration of artificial intelligence, machine learning, and medical image processing.
