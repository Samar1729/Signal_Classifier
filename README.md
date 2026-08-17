#  Intelligent Signal Classifier

An AI-powered signal modulation classification system built using **Deep Learning, TensorFlow/Keras, and Streamlit**. The application classifies wireless communication signals from IQ samples and predicts the modulation type with confidence scores through an interactive web interface.

---

##  Features

-  Automatic modulation classification
- Deep Learning model using TensorFlow/Keras
- Upload `.npy` IQ signal files
- Displays prediction confidence
-  Probability distribution for all modulation classes
-  Interactive Streamlit interface
-  Fast real-time inference

---

## 🛠️ Tech Stack

- Python
- TensorFlow / Keras
- Streamlit
- NumPy
- Matplotlib (optional)

---

##  Repository Structure

```
.
├── main.py                 # Streamlit application
├── bmc1.ipynb              # Model training notebook
├── bmc_input.ipynb         # Data preprocessing & input preparation
├── signal_classifier.h5    # Trained model (not included)
├── README.md
└── requirements.txt
```

---

##  Supported Signal Classes

The model can classify the following **24 modulation schemes**:

| Digital | Analog |
|---------|---------|
| OOK | FM |
| 4ASK | AM-SSB-WC |
| 8ASK | AM-SSB-SC |
| BPSK | AM-DSB-WC |
| QPSK | AM-DSB-SC |
| 8PSK | |
| 16PSK | |
| 32PSK | |
| 16APSK | |
| 32APSK | |
| 64APSK | |
| 128APSK | |
| 16QAM | |
| 32QAM | |
| 64QAM | |
| 128QAM | |
| 256QAM | |
| GMSK | |
| OQPSK | |

---

## ⚙️ Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/intelligent-signal-classifier.git
```

```bash
cd intelligent-signal-classifier
```

---

### Create Virtual Environment

Windows

```bash
python -m venv venv
```

Activate

```bash
venv\Scripts\activate
```

Linux/Mac

```bash
python3 -m venv venv
source venv/bin/activate
```

---

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

##  Run the Application

```bash
streamlit run main.py
```

After running, open

```
http://localhost:8501
```

---

##  Input Format

Upload a NumPy file (`.npy`) having the following shape:

```
(2,1024)
```

where

- Row 1 → In-phase (I)
- Row 2 → Quadrature (Q)

If the uploaded file has shape

```
(1024,2)
```

the application automatically transposes it.

---

##  Output

The application displays:

- Predicted modulation type
- Prediction confidence (%)
- Probability distribution across all classes

---

##  Model

The trained model is built using **TensorFlow/Keras** and loaded during application startup. It classifies uploaded IQ signal samples into one of the supported modulation schemes before displaying the predicted class and confidence score. :contentReference[oaicite:0]{index=0}

---

##  User Interface

The Streamlit interface allows users to:

- Upload IQ signal files
- Validate input shape
- Predict modulation type
- View confidence score
- Visualize prediction probabilities using a bar chart :contentReference[oaicite:1]{index=1}

---

## Future Improvements

- CNN + Transformer architecture
- Support additional modulation schemes
- Live SDR (Software Defined Radio) integration
- Signal visualization before prediction
- ONNX/TensorRT deployment
- Docker deployment
- Cloud deployment

---

##  Author

**Shashi Bhushan Raj**

B.Tech Electronics & Communication Engineering

**Interests**

- Artificial Intelligence
- Deep Learning
- Wireless Communication
- Signal Processing
- Machine Learning

---

