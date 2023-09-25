# Redis Cluster Helm Chart
This repository contains a Helm chart to deploy a Redis cluster in a Kubernetes environment. The chart is designed to provide a scalable Redis setup with options for replication and persistence.

# Usage
Follow these steps to deploy the Redis cluster using this Helm chart.

## Step 1: Helm Chart Structure
Ensure the folder structure follows the Helm chart convention:
```
redis-cluster-helm-chart/
  Chart.yaml
  values.yaml
  templates/
    tests
    deployment.yaml
    config.yaml
    statefulset.yaml
    ingress
    hpa

``` 
## Step 2: Chart.yaml
The Chart.yaml file contains metadata about the Helm chart.

## Step 3: values.yaml
Customize default values for the Redis cluster configuration in the values.yaml file.

## Step 4: ConfigMap
Create a ConfigMap (configmap.yaml) to hold Redis configuration.

## Step 5: StatefulSet
Define a StatefulSet (redis-cluster-statefulset.yaml) to manage Redis instances.

# Installation
1. Customize the values in values.yaml to tailor the Redis cluster configuration according to your requirements.

2. Install the Helm chart using the following command:

```
helm install redis-cluster redis-cluster-helm-chart/
```
Replace redis-cluster with your desired release name.

3. Verify the deployment using kubectl commands, such as kubectl get pods.

# Customization
Modify the configuration files to suit your specific needs, such as adjusting the number of Redis replicas, enabling persistence, or configuring Redis settings.

# Support and Contribution
For any issues or concerns, please open an issue. Contributions and improvements are welcome; feel free to create a pull request.
