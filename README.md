# REAIL — AI Image Detector

REAIL is a Streamlit web application that detects whether an image is real or AI-generated using a MobileNetV2 transfer learning model trained on the CIFAKE dataset.

## Features
- **Instant Image Classification**: Predicts Real vs. AI-Generated with confidence scores.
- **Dark Modern Theme**: Built with a custom styled Streamlit interface.
- **User Authentication**: Account registration and login system with SHA-256 password hashing.
- **Daily Quotas**: 5 uploads/day for free users, unlimited for Admin.
- **Model Caching**: Uses `@st.cache_resource` for low-latency inference without reloading model weights on each interaction.

## Project Structure
```text
├── app.py                # Main Streamlit application
├── requirements.txt      # Dependencies for Streamlit Cloud
├── users.json            # Local user credentials store
├── detector.h5           # Trained MobileNetV2 Keras model
├── LOGO.jpg              # App logo (optional)
├── .streamlit/
│   └── config.toml       # Streamlit theme and server configuration
└── .gitignore            # Git ignore rules
```

## Running Locally
1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   cd <your-repo-name>
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Place `detector.h5` and `LOGO.jpg` in the root folder.
4. Run the app:
   ```bash
   streamlit run app.py
   ```

## Default Admin Credentials
- **Username**: `admin`
- **Password**: `admin123`
