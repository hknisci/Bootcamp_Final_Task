# My Node.js App

This is a simple Node.js application with an Express server, containerized using Docker, and deployed on Kubernetes.

## Prerequisites

- Node.js and npm
- Docker
- Kubernetes (Minikube)
- Jenkins
- Helm (for Prometheus and Grafana setup)

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/hknisci/Bootcamp_Final_Task.git)](https://github.com/hknisci/Bootcamp_Final_Task.git
   cd my_node_app
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

## Running the Application Locally

1. Start the application:
   ```bash
   npm start
   ```

2. Open your browser and navigate to `http://localhost:3000`.

## Dockerization

1. Build the Docker image:
   ```bash
   docker build -t my_node_app .
   ```

2. Run the Docker container:
   ```bash
   docker run -p 3000:3000 my_node_app
   ```

## Kubernetes Deployment

1. Start Minikube:
   ```bash
   minikube start
   ```

2. Deploy the application:
   ```bash
   kubectl apply -f k8s/deployment.yaml
   kubectl apply -f k8s/service.yaml
   ```

3. Access the application:
   ```bash
   minikube service my-node-app-service
   ```

## CI/CD Pipeline with Jenkins

1. Set up Jenkins and create a new pipeline project.
2. Use the `Jenkinsfile` in this repository to configure the pipeline.

## Monitoring with Prometheus and Grafana

1. Install Prometheus:
   ```bash
   kubectl create namespace monitoring
   helm install prometheus stable/prometheus --namespace monitoring
   ```

2. Install Grafana:
   ```bash
   helm install grafana stable/grafana --namespace monitoring
   ```

3. Access Grafana and create dashboards to visualize metrics.


# Bootcamp_Final_Task
