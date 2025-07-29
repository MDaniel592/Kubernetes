
kubectl create namespace squid
kubectl create configmap squid-config --from-file=squid=squid.conf --namespace squid
kubectl apply -f squid.yaml --namespace squid
kubectl get all -n squid