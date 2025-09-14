# ecommerce-helm-charts
Helm charts for deploying the Ecommerce microservices application (MongoDB, MySQL, Catalogue, and Redis) on Kubernetes.

# 📦 Ecommerce Helm Charts

This repository contains **Helm charts** to deploy the **Ecommerce microservices application** on Kubernetes.  
It includes charts for the following core services:  
- **MongoDB** (NoSQL database for product/catalogue data)  
- **MySQL** (Relational database for orders)  
- **Catalogue Service** (Node.js service serving product catalogue)  
- **Redis** (In-memory cache for sessions)  

# EBS Install drivers with Helm
-------------------------
Add the aws-ebs-csi-driver Helm repository.

    helm repo add aws-ebs-csi-driver https://kubernetes-sigs.github.io/aws-ebs-csi-driver
    helm repo update

Install the latest release of the driver.

    helm upgrade --install aws-ebs-csi-driver \
        --namespace kube-system \
        aws-ebs-csi-driver/aws-ebs-csi-driver