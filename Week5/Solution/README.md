# WORK IN PROGRESS
# Solution to setup Continuous monitoring, logging and alerting on Kubernetes cluster using opensource tools

## If you are a video person, feel free to check out the below video for end to end solution:


## If you are a documentation reader, feel free to follow the below steps:

## Steps to be performed:
*  Setup a Kubernetes cluster
*  Helm installation
*  Deploy Opensource Prometheus using Helm
*  Deploy a sample application to the cluster
*  Setup metrics server using Helm
*  Setup metrics based alerts
*  Setup Grafana dashboard
*  Install Grafana using Helm
*  EFK stack setup
*  Logging Setup

## Create a GKE cluster using gcloud
```bash
  gcloud container clusters create-auto thecloudopscommunity \
    --release-channel=stable \
    --region=us-east1
 ```

## Helm installation

```bash
curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
chmod 700 get_helm.sh
./get_helm.sh
```
## Deploy Prometheus and Grafana

```bash
helm repo add bitnami https://charts.bitnami.com/bitnami
helm install tutorial bitnami/kube-prometheus \
--version 8.2.2 \
--values extras/prometheus/oss/values.yaml \
--wait

helm repo add grafana https://grafana.github.io/helm-charts
helm repo update
helm install my-release grafana/grafana

```

## Deploy sample application Bank of Anthos
```bash
git clone https://github.com/GoogleCloudPlatform/bank-of-anthos.git
cd bank-of-anthos/
kubectl apply -f extras/jwt/jwt-secret.yaml
kubectl apply -f kubernetes-manifests
```

## Setup Metrics Server
```
helm repo add metrics-server https://kubernetes-sigs.github.io/metrics-server/
helm upgrade --install metrics-server metrics-server/metrics-server
```

## Configure Slack

## Configure Alert manager
```
kubectl create secret generic alertmanager-slack-webhook --from-literal webhookURL=SLACK_WEBHOOK_URL
kubectl apply -f extras/prometheus/oss/alertmanagerconfig.yaml
```

### Configure Prometheus
```
kubectl apply -f extras/prometheus/oss/probes.yaml
kubectl apply -f extras/prometheus/oss/rules.yaml
```






