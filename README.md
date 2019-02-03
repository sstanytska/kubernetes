# kubernetes

#1)  Run uname command in a single busybox container.The command should run every minute and must complete, within 10 seconds or be terminated by Kubernetes. The cronjob name and container should be hello.

vim cronjon.yaml
kubectl create -f cronjob.yaml
kubectl get cronjob
kubectl get jobs

# 2 Troubleshoot Applications
https://kubernetes.io/docs/tasks/debug-application-cluster/debug-application/
# 3 Create a pod named myapp wit 4 containers, using nginx, redis, memchached, consul images.
vim myapp.yaml

kubectl create -f myapp.yaml
# 4 Find the pod which is using the most CPU resources and pipe the name to report.txt file
kubectl top pods | grep myapp.yaml  >> report.txt

# 5 Create new pod, from redis image, running in web namespace and listening at port 9090. * Create a namespace if doest exist.
vim redis-pod.yaml
kubectl create namespace web;  
kubectl get namespaces  
kubectl create -f redis-pod.yaml  

# 6 Create a pod in test namespace and set resource limit 1G of memmory and 200m CPU. * Create a namespace if doest exist.
vim test-pod.yaml 
kubectl create namespace test;  
kubectl create -f test-pod.yaml;  
kubectl get pods;  
