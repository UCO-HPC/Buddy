# Foreman

Based on this project: https://github.com/ohadlevy/foreman-kube

## Install
1. ``cp values.yaml.example my_values.yaml`` and configure it
2. Install with ``helm install -f my_values.yaml --namespace my-foreman my-foreman chart``