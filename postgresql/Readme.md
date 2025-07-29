
kubectl create namespace postgresql
<!-- kubectl create configmap pg-hba-config --from-file=postgresql=pg_hba.conf --namespace postgresql
kubectl create configmap postgresql-config --from-file=postgresql=postgresql.conf --namespace postgresql -->
kubectl create -f postgres-config.yaml
kubectl apply -f postgresql.yaml --namespace postgresql
kubectl get all -n postgresql