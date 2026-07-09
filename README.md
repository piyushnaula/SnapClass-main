# SnapClass - AI Powered Attendance System (Streamlit App)

SnapClass is an advanced attendance management system utilizing AI for facial and voice recognition. This Streamlit application serves as the core platform where teachers and students can manage courses, enroll using biometrics, and track attendance seamlessly.

## Features
- **Teacher Dashboard**: Manage subjects, view attendance logs, and generate join codes.
- **Student Dashboard**: Track personal attendance across enrolled subjects.
- **Biometric Enrollment**: Register face and voice biometrics for secure identification.
- **AI Attendance**: Conduct attendance using either facial recognition (FaceID) or sequential voice ID.
- **QR Code Joining**: Generate QR codes for instant student enrollment to courses.

## Tech Stack
- **Frontend & Backend**: Streamlit (Python)
- **Database**: Supabase (PostgreSQL)
- **Face Recognition**: `face_recognition`, `dlib`
- **Voice Recognition**: `Resemblyzer`, `librosa`
- **Other Utilities**: `bcrypt`, `segno` (QR Codes)

## How to Run Locally

### Prerequisites
- Python 3.8+
- Supabase account (for database setup)

### Setup Steps

1. **Navigate to the app directory**
   ```bash
   cd ai-attendance-project-app-main
   ```

2. **Install Dependencies**
   It's recommended to use a virtual environment.
   ```bash
   pip install -r requirements.txt
   ```
   *Note: Installing `dlib` might require CMake and Visual Studio C++ Build Tools on Windows.*

3. **Configure Environment Variables**
   Create a `.streamlit/secrets.toml` file in the root directory (already created for you):
   ```toml
   SUPABASE_URL = "your-supabase-url"
   SUPABASE_KEY = "your-supabase-anon-key"
   ```
   *(You can find these in your Supabase project under Settings -> API)*

4. **Run the Application**
   ```bash
   streamlit run app.py
   ```
   The app will start at `http://localhost:8501`.

## Connecting with the Landing Page
This project works alongside the `ai-attendance-project-landing-main` project. The landing page acts as a marketing frontend which redirects users to this Streamlit application. Make sure to update the URLs in the landing page if you are running this locally.