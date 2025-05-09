EndomorphineEdge- A Women’s Fitness Tracker App
----------------------------

Created by: Anvisha Chopra  
Age: 20  
University: Deakin University
SIT323 Project: Task 10.2HD

INTRODUCTION
-------------
The Women’s Fitness Tracker App is a cloud-native web application designed exclusively for women to track their fitness progress, workout history, personal health data, analytics, goals, achievements, and more. As a passionate fitness enthusiast, I created this app to serve as a safe, encouraging, and empowering space for women. 

From color choices (pink and white) to design elements, every detail reflects the app’s purpose: uplifting and supporting women on their unique health journeys.

WHAT'S INCLUDED
----------------
The app has two main components:

1. **Frontend (Client Side):**  
   HTML, CSS, and JavaScript pages like:
   

2. **Backend (Server Side):**  
   A Node.js server (`server.js`) that handles data processing, storage (in memory or connected DB), and routes.

3. **Containerization & Deployment:**
   - Docker used to package the backend.
   - GCP (Google Cloud Platform) used for deployment via Kubernetes and Google Container Registry.

HOW TO RUN LOCALLY
-------------------
Step 1: BACKEND  
Navigate to the backend directory and run:

    cd backend
    npm install
    node server.js

The backend server will be running at:

    http://localhost:5000

Step 2: FRONTEND  
Navigate to the frontend directory and start a simple HTTP server using Python:

    cd frontend
    python -m http.server 8000

Access the app at:

    http://localhost:8000

DOCKERIZATION
---------------
To containerize the backend:

1. Create a Dockerfile in the root/backend folder.
2. Craeted a Dockerfile    
3. Build and run Docker image:

    docker build -t endomorphineedge
    docker run -p 5000:5000 endomorphineedge

CLOUD DEPLOYMENT ON GCP
-------------------------
Step-by-step deployment process:

1. Set up a Google Cloud Platform account and created a new project.
2. Enabled the following APIs:
   - Kubernetes Engine API
   - Container Registry API
   - Cloud Storage API
   - Cloud Monitoring API
   - Cloud Logging API

3. Authenticated with GCP and set project ID

4. Built Docker image and pushed it to GCR

5. Created a Kubernetes cluster

6. Deployed the app to Kubernetes

7. Wait for the external IP to be assigned and access your app via:

    kubectl get service

Final Message from the creator of the App
---------------
I hope this app brings together technology, design, and purpose to promote women’s fitness journeys in a meaningful and respectful way. Whether for personal growth, health tracking, or motivation, this app is a step toward inclusive fitness technology.

