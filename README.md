# Verita: Multi-Modal Biometric AI Attendance Infrastructure

[![Live Demo](https://img.shields.io/badge/Demo-Vercel-blue?style=for-the-badge)](https://verita-landing-page-rose.vercel.app)
[![Engine](https://img.shields.io/badge/ML_Engine-Streamlit-FF4B4B?style=for-the-badge)](https://verita-main.streamlit.app/)

Verita is an enterprise-grade, multi-modal biometric attendance infrastructure designed to modernize classroom verification workflows. By pairing high-fidelity computer vision architectures with digital signal processing vocal biometrics, Verita eliminates proxy-attendance vulnerabilities while processing student rosters concurrently.

The architecture decouples the high-performance ML microservices from the public web orientation, relying on a lightweight Flask edge layer to optimize initial load speeds and web vitals before routing transactions to the core execution environment.

---

## 🚀 Machine Learning Core Architecture

### 📸 Face ID Pipeline (Computer Vision Core)

* **Feature Extraction:** Utilizing `Dlib` deep metric learning pipelines to localize facial structural landmarks and compute absolute **128-dimensional vector embeddings** per entity.
* **Vectorized Inference:** High-speed matrix computation powered by the `FaceRecognition` engine to isolate, tag, and cross-reference multiple student entities simultaneously from a single, uncalibrated room viewport sweep.
* **Tolerance Handling:** Configured strict cosine distance threshold vectors to successfully evaluate under extreme variations in room illumination, head tilt angles, and low-light sensor captures.

### 🎙️ Voice ID Pipeline (Digital Signal Processing & Audio AI)

* **Feature Engineering:** Extracting Mel-Frequency Cepstral Coefficients (MFCCs), spectral roll-off, and chroma variants using `Librosa` to isolate ambient noise signals from unique audio tracks.
* **Biometric Verification:** Layering `Resemblyzer` speaker-discriminative neural network topologies to transform raw voice sequences into standardized vocal signature embeddings.
* **Real-Time Evaluation:** Employs concurrent distance matrix comparisons to score sequentially spoken "Present" responses against multi-session voice enrollment indices.

### ⚡ Distributed System & Data Engineering

* **Data Layer:** Cloud-native relational topologies built securely across a high-availability Postgres backend hosted on `Supabase`.
* **State Sync:** Thread-safe transition pools passing session tokens between the Flask landing layer and reactive Streamlit worker loops asynchronously.

---

## 🗺️ Functional Core Workflows

The platform scales operations across two isolated system perspectives:

### 👨‍🏫 The Teacher Portal Workflow

1. **Secure Session Initiation:** Multi-factor authentication layer logging into an encrypted subject roster node.
2. **Dynamic Dashboard Telemetry:** Real-time visibility into subject rosters, confidence scoring metrics, and transaction logs.
3. **Computer Vision Scanning:** One-click spatial evaluation via class photo arrays mapping face vector matching matrices instantly.
4. **Vocal Signature Roll-Call:** Real-time stream processing mapping confidence rankings to the live ledger.
5. **Data Export:** Instant compiling of system states to downloadable immutable `.csv` reports.

### 👨‍🎓 The Student Onboarding Workflow

1. **QR Roster Enrollment:** High-speed classroom registration binding unique device identities directly to server course nodes.
2. **Biometric Registration:** Direct secure pipeline capturing baseline face and voice vectors into Supabase.
3. **Timeline Evaluation:** Access to transparent personal logging streams highlighting exact biometric confidence check scores.

---

## 🛠️ Infrastructure Overview

[ Public Flask Web Gateway ] ────► [ Streamlit Machine Learning Processing Layer ]
│                        │
┌─────────────────────────┘                        └────────────────────────┐
▼                                                                           ▼
[ Vision Architecture (Dlib) ]                                           [ Audio AI Core (Resemblyzer) ]
└─► 128-D Vector Embeddings                                              └─► Voice Verification Embeddings
│                                                                                 │
└─────────────────────────┬───────────────────────────────────────────────────────┘
▼
[ Cloud Storage Infrastructure (Supabase) ]


---
## 📦 Installation & Local Development Setup

To initialize and evaluate the project dependencies locally, establish isolated runtime boundaries:

### Prerequisites
* Python 3.9+
* Active Git terminal instance
* C++ CMake Compiler (Required for compilation of local Dlib vector modules)

### Step-by-Step Configuration

1. **Clone the Repository:**
   ```bash
   git clone [https://github.com/sumitstat07/verita-landing-page.git](https://github.com/sumitstat07/verita-landing-page.git)
   cd verita-landing-page
Initialize Isolated Virtual Environment:

Bash
python -m venv venv

# Activate on Linux/MacOS
source venv/bin/activate

# Activate on Windows PowerShell
.\venv\Scripts\Activate.ps1
Install Package Dependencies:

Bash
pip install --upgrade pip
pip install -r requirements.txt
Boot the Edge Server Environment:

Bash
python app.py
The routing interface will expose a local runtime boundary at http://127.0.0.1:5000.

📈 Engineering Commit Integrity
This codebase utilizes the Conventional Commits engineering standard to preserve clear operational workflows:

feat(cv): Implementation additions regarding Face ID or image evaluation code blocks.

feat(audio): Digital Signal Processing pipeline changes or voice vector metrics.

fix(infrastructure): Addressing hosting configuration issues or static server asset 404 errors.

style(ux): Refining frontend layouts, visual alignments, or responsive fluid sizing breaks.


