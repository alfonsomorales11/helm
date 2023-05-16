# Package a helm chart
```
helm package stride-chart
```

# Move generated .tgz file to charts folder
```
mv ./stride-chart/stride-chart-0.1.1.tgz ./charts/
```

# Generate index.yaml file
```
helm repo index .
```

# Add a new helm repository
```
helm search repo alfonsomorales11
```

# Search for available charts in a repository
```
helm search repo alfonsomorales11
```

# Install helm chart as it is
```
helm install stride  alfonsomorales11/stride-chart
```

# Install helm chart & override values
```
helm install stride --set deploymentName="mydeploy" alfonsomorales11/stride-chart
```
***

# Install helm chart

```
helm install stride alfonsomorales11/stride-chart --set-string namespace.name=$NAMESPACE --set-string deploymentName=$DEPLOYMENT_NAME --set-string repositoryURL=$NEXUS_URL --set-string dockerConfig.value=$DOCKER_CONFIG_VALUE --set-string image.name=$IMAGE_NAME --set-string image.tag=$BUILD_NUMBER --set-string secretName=$SECRET_NAME

helm upgrade stride alfonsomorales11/stride-chart --set-string namespace.name=$NAMESPACE --set-string deploymentName=$DEPLOYMENT_NAME --set-string repositoryURL=$NEXUS_URL --set-string dockerConfig.value=$DOCKER_CONFIG_VALUE --set-string image.name=$IMAGE_NAME --set-string image.tag=$BUILD_NUMBER --set-string secretName=$SECRET_NAMEt
```