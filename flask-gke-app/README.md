# Flask GKE App

This project is a simple Flask application deployed on Google Kubernetes Engine (GKE). It demonstrates how to containerize a Flask app and manage its deployment using Kubernetes.

## Project Structure

```
flask-gke-app
├── src
│   └── app.py                # Main Flask application
├── k8s
│   ├── deployment.yml        # Kubernetes deployment configuration
│   ├── kustomization.yml      # Kustomization file for managing Kubernetes resources
│   └── service.yml           # Kubernetes service configuration
├── requirements.txt          # Python dependencies
├── Dockerfile                 # Dockerfile for building the Flask app image
└── README.md                  # Project documentation
```

## Setup Instructions

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd flask-gke-app
   ```

2. **Install dependencies:**
   Make sure you have Python and pip installed, then run:
   ```bash
   pip install -r requirements.txt
   ```

3. **Build the Docker image:**
   ```bash
   docker build -t flask-gke-app .
   ```

4. **Deploy to GKE:**
   - Ensure you have `kubectl` configured to communicate with your GKE cluster.
   - Apply the Kubernetes configurations:
     ```bash
     kubectl apply -k k8s/
     ```

5. **Access the application:**
   - If using a LoadBalancer service, get the external IP:
     ```bash
     kubectl get services
     ```
   - Open your browser and navigate to `http://<external-ip>:5000`.

## Usage

The Flask application responds with "Hello, World!!" when accessed at the root URL (`/`). You can modify `src/app.py` to change the behavior of the application.

## License

This project is licensed under the MIT License.