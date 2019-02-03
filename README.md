# kubernetes

#1) vim cronjon.yaml
kubectl create -f cronjob.yaml
kubectl get cronjob
kubectl get jobs

# 2 Troubleshoot Applications
https://kubernetes.io/docs/tasks/debug-application-cluster/debug-application/
# 3
vim myapp.yaml

kubectl create -f myapp.yaml
# 4
kubectl top pods | grep myapp.yaml  >> report.txt

# 5 vim redis-pod.yaml
kubectl create namespace web
kubectl get namespaces
kubectl create -f redis-pod.yaml

# 6 vim test-pod.yaml
kubectl create namespace test
kubectl create -f test-pod.yaml
kubectl get pods
