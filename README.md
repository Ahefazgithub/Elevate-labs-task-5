# Kubernetes Minikube Deployment on EC2

## 📋 Project Summary

This project demonstrates how to deploy and manage a containerized application using a local Kubernetes cluster with Minikube on an AWS EC2 instance.

### 🚀 Objective
- Build a local Kubernetes cluster using Minikube
- Deploy an NGINX application using a Deployment YAML
- Expose the application using a NodePort Service
- Scale and manage the application with `kubectl` commands
- Verify functionality using pod and service listings

### 🔧 Tools & Technologies
- EC2 Instance (Amazon Linux 2)
- Minikube
- kubectl
- Docker
- Git & GitHub

### ✅ Steps Performed

1. **Provisioned EC2 Instance**  
   - Launched a `t2.medium` EC2 instance with Amazon Linux 2  
   - Connected via PuTTY

2. **Installed Dependencies**  
   - Installed Docker, kubectl, and Minikube  
   - Started Docker and Minikube using the Docker driver

3. **Created Kubernetes YAML files**
   - `deployment.yaml`: NGINX deployment with 2 replicas  
   - `service.yaml`: NodePort service exposing NGINX on port 30080

4. **Applied Configuration**
   - Deployed resources using `kubectl apply -f`  
   - Verified with `kubectl get pods`, `kubectl get svc`

5. **Managed Application**
   - Scaled deployment to 4 replicas  
   - Described pods and viewed logs

6. **Documented Output**
   - Took screenshots of pod/service states  
   - Documented steps in this `README.md`

7. **Pushed to GitHub**
   - Initialized a Git repo  
   - Committed all files and pushed to GitHub repository

### 📁 Files Included
- `deployment.yaml`
- `service.yaml`
- `README.md`




[ec2-user@ip-172-31-34-157 ~]$ kubectl get pods
kubectl get svc
NAME                                READY   STATUS    RESTARTS   AGE
myapp-deployment-58dbdb69b8-kcnsp   1/1     Running   0          7m30s
myapp-deployment-58dbdb69b8-n68q8   1/1     Running   0          6m41s
myapp-deployment-58dbdb69b8-p8h49   1/1     Running   0          6m41s
myapp-deployment-58dbdb69b8-xqph9   1/1     Running   0          7m30s
NAME            TYPE        CLUSTER-IP     EXTERNAL-IP   PORT(S)        AGE
kubernetes      ClusterIP   10.96.0.1      <none>        443/TCP        12m
myapp-service   NodePort    10.108.7.242   <none>        80:30080/TCP   7m21s
[ec2-user@ip-172-31-34-157 ~]$


