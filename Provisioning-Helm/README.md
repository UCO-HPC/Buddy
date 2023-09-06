# Foreman

Based on this project: https://github.com/ohadlevy/foreman-kube

## Install
1. ``cp values.yaml.example my_values.yaml`` and configure it
2. Install with ``helm install -f my_values.yaml --namespace foreman foreman chart``
3. Run the following command to initialize database: ``kubectl exec -it --namespace foreman jobs.batch/setup -- bash -c "bundle exec rake db:create db:migrage db:seed"``
4. Delete setup job: ``kubectl delete jobs --namespace foreman setup``
