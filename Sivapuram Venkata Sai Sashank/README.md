# 📒 AI Trace Finder: Scanner ID Pipeline with Flatfield Fingerprints

This project implements a **scanner identification pipeline** that
extracts **unique scanner fingerprints** from flat-field images and uses
them to detect the source of scanned documents. The workflow combines
**signal processing, Fourier analysis, and machine learning (SVM, CNN,
Random Forest, XGBoost)** for accurate scanner classification.

------------------------------------------------------------------------

## 🚀 Features

-   📂 **Flatfield Fingerprint Extraction** -- derive scanner-specific
    noise patterns from flat images.\
-   🧾 **Document Residual Analysis** -- isolate scanner noise in
    scanned documents.\
-   🔬 **FFT Feature Engineering** -- extract frequency-domain features
    for classification.\
-   🤖 **Machine Learning Models** -- includes SVM, CNN, Random Forest,
    and XGBoost classifiers.\
-   📊 **Evaluation Tools** -- confusion matrix, accuracy reports, and
    visualizations.\
-   💾 **Model Persistence** -- save and load models with `joblib`.

------------------------------------------------------------------------

## Data set links

-   Flatfield images : https://drive.google.com/drive/folders/11t9KQyRbchzaPQ5ZaGsEfxVkfeP9Umro?usp=sharing 
-   Official documents scans : https://drive.google.com/drive/folders/15ZMfNcfLZpYgCQBLSNopFd6x69CKiZSv?usp=sharing 
-   Wikipedia documents scans : https://drive.google.com/drive/folders/1rZaGDLczp9SUvEX1AOW6ljxf4vvQFS12?usp=sharing.

------------------------------------------------------------------------

## 📂 Project Workflow

1.  **Build Flatfield Fingerprints**\
    Extract unique noise signatures from reference flat-field images.

2.  **Extract Document Residuals**\
    Apply denoising and FFT transforms to capture scanner artifacts.

3.  **Correlate Residuals with Fingerprints**\
    Measure similarity using correlation and frequency-domain metrics.

4.  **Train Classifiers**

    -   Train traditional ML (SVM, Random Forest, XGBoost).\
    -   Train deep learning models (CNN with PyTorch).

5.  **Evaluate Performance**\
    Compare classifiers with accuracy, confusion matrix, and feature
    importance.

------------------------------------------------------------------------

## 📦 Installation

Clone the repository and install dependencies:

``` bash
git clone https://github.com/yourusername/AI_Trace_Finder.git
cd AI_Trace_Finder
pip install -r requirements.txt
```

### Requirements

-   Python 3.8+
-   NumPy, SciPy, Matplotlib
-   scikit-image
-   scikit-learn
-   PyTorch
-   joblib
-   XGBoost

------------------------------------------------------------------------

## 🛠 Usage

1.  **Set dataset paths** inside the notebook or config file:

``` python
FLATROOT = "path/to/flatfields"
OFFICIALROOT = "path/to/official_docs"
WIKIROOT = "path/to/wiki_docs"
```

2.  **Run the notebook** to execute the pipeline:

``` bash
jupyter notebook AI_Trace_Finder.ipynb
```

3.  **Train & Save Model**\
    Models will be trained and saved as `.pkl` or `.pth` files.

4.  **Evaluate**\
    Confusion matrix and classification reports will be generated.

------------------------------------------------------------------------

## 📊 Example Results

-   Fingerprint images in the frequency domain.\
-   Confusion matrix of classifier performance.\
-   Accuracy scores for SVM, CNN, Random Forest, and XGBoost.

*(Add screenshots/plots here for better presentation)*

------------------------------------------------------------------------

## 📂 Repository Structure

    AI_Trace_Finder/
    │── AI_Trace_Finder.ipynb   # Main notebook
    │── data/                   # Dataset folder
    │   ├── flatfields/         
    │   ├── Official/           
    │   └── Wikipedia/          
    │── models/                 # Saved ML models
    │── requirements.txt         # Dependencies
    │── README.md               # Project documentation

------------------------------------------------------------------------

## 🔮 Future Work

-   Expand dataset with more scanners.\
-   Optimize CNN architecture for better generalization.\
-   Develop a CLI tool for real-time scanner identification.\
-   Deploy as a web service/API for forensic document analysis.

------------------------------------------------------------------------

## 👨‍💻 Author

Developed as part of a research pipeline for **document forensic
analysis**.\
Feel free to contribute via pull requests or open issues.
