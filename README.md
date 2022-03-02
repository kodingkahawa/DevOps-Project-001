# DevOps-Project-001
The project involves building a complete automated deployment

# Problem Statement
1. Build a complete automated deployment for a web app residing in a GitHub repository into a Kubernetes Cluster hosted on a cloud platform. The web app should have a url so that public users can access it.
2. Add autoscaling to handle unexpected load whereby the cluster determines the load and scales up web apps horizontally.
3. Deploy a single monitoring tool to monitor and visualize the cluster.

# Setup
1. Using a remote Jenkins Automation Server running on my local machine. The Jenkins Server is configured with docker and kubectl.
2. Install Docker Pipeline and Google Kubernetes Engine plugins.
3. Create a kubernetes cluster with Google Kubernetes Engine on the Google Cloud Platform
4. Configure credentials on the Jenkins Server that allows it to authenticate into GKE using Service Account, configure credentials for GitHub Repo and Docker Hub
5. Keep Dockerfile, Jenkinsfile, deployment.yaml and application files on the GitHub repository.
6. Dockerfile contains the instructions on how to containerize the application
7. deployment.yaml contains the kubernetes manifest files that define how to deploy the application from docker hub unto the kubernetes cluster.
8. Jenkinsfile contains the following 5 stages; Checkout, Build, Test, Push Image, Deploy to GKE
9. Configure build triggers for the GitHub Repository to automatically build and deploy to the kubernetes test cluster and then wait for approval for the deployment unto the production cluster
10. Implement Autoscaling using HorizontalPodAutoscaler(k8s) for pods and Cluster Autoscaler(cloud platform)
11. Using Helm install/deploy Prometheus and Grafana to kubernetes cluster, configure them to monitor the cluster

