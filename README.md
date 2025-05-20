# Flask Docker Example

This is a minimal Flask application running in a Docker container.

## Getting Started

### Prerequisites
- Docker installed
- Python 3.11+ (for local development)

### Running with Docker
1. Build the Docker image:
   ```powershell
   docker build -t flask-docker-app .
   ```
2. Run the container:
   ```powershell
   docker run -p 5000:5000 flask-docker-app
   ```
3. Open your browser and go to http://localhost:5000

### Running Locally (without Docker)
1. Create and activate a virtual environment:
   ```powershell
   python -m venv .venv
   .venv\Scripts\Activate.ps1
   ```
2. Install dependencies:
   ```powershell
   pip install -r requirements.txt
   ```
3. Run the app:
   ```powershell
   python app.py
   ```

## Project Structure
- `app.py` - Main Flask application
- `requirements.txt` - Python dependencies
- `Dockerfile` - Docker build instructions
- `.dockerignore` - Files to ignore in Docker builds
- `.gitignore` - Files to ignore in git

---

This project was generated with GitHub Copilot.
