# Deploying PHPMyAdmin application using Helm Chart

Let's learn How to deploy PHPMyAdmin application using helm chart? Learn more about helm [here](https://helm.sh/).

## Prerequisites:

### Create NFS share
Reference:
- https://www.linuxbabe.com/ubuntu/nfs-share
- https://vitux.com/install-nfs-server-and-client-on-ubuntu/

### Install Helm
Refer installation guide [here](https://helm.sh/docs/intro/install/)

### Go to session_5 directory
```
cd ../session_5/
```

## Step 1: Create PHPMyAdmin helm chart
```
helm create phpmyadmin
```

## Step 2: Add all application YAML files to templates directory
Remove unwanted files from template directory
```
rm -rf ./phpmyadmin/templates/*
```
Copy YAML files
```
cp configmap.yaml db-deployment.yaml db-pv.yaml db-pvc.yaml db-service.yaml secret.yaml phpmyadmin-deployment.yaml phpmyadmin-ingress.yaml phpmyadmin-service.yaml ./phpmyadmin/templates/
```