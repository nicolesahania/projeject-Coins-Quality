# Coin Quality Detection — Vendo Machine Scanner

Automated coin quality inspection system for vendo machines. Uses CNN + OpenCV to detect defects (Rusty, Damaged, Scratched) and gives a clear **SAFE TO USE** or **DO NOT INSERT** verdict.

## How to Run

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. (Optional) Add your trained model

Place your `multi_feature_coin_model_FINAL.keras` file in the project root. The app works without it using OpenCV-only analysis.

### 3. Start the app

```bash
streamlit run coin_ui.py
```

The app opens at `http://localhost:8501`.

## Features

| Feature | Description |
|---|---|
| **Binary Verdict** | One clear answer: green **SAFE TO USE** or red **DO NOT INSERT** |
| **Auto Scan** | Scan triggers automatically when a coin image is loaded — no extra button clicks |
| **Camera Capture** | Use your device camera to snap coins directly |
| **Batch Mode** | Switch to "Batch / Continuous" to scan many coins and track pass/fail stats |
| **Defect Details** | When rejected, shows which defects were found (Rusty, Damaged, Scratched) |

## Scan Modes

- **Single Scan** — Upload or capture one coin, get instant verdict
- **Batch / Continuous** — Scan multiple coins in sequence; the app tracks totals, passes, and rejects with a scrollable history log

## Tech Stack

- **Streamlit** — UI framework
- **TensorFlow / Keras** — CNN model inference
- **OpenCV** — Image preprocessing and surface analysis
- **Pillow** — Image handling
