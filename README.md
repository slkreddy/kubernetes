# kubernetes
kubectl run nginx --image=nginx




namespaces:

kubectl get namespace
kubectl get pods --all-namespaces

kubectl get all --all-namespaces

get al deploys:
kubectl get deploy --all-namespaces


Gives Pod and Node info
--------------------------
kubectl get pods -o wide

Serialize pod def to local yaml
----------------------
kubectl get pod simple-webapp-2  -o yaml > webapp-2.yaml



logs---
-----
kubectl logs -f my-pod                              # stream pod logs (stdout)
kubectl logs my-pod -c my-container                 # dump pod container logs (stdout, multi-container case)


Monitoring

kubectl top node
kubectl top pods

Run the command 'kubectl get all --selector env=prod'


INGRESS:

kubectl describe ingress --namespace app-space
kubectl edit ingress --namespace app-space


kubectl get deploy --all-namespaces


kubectl create namespace ingress-space
kubectl create configmap nginx-configuration --namespace ingress-space
kubectl create serviceaccount ingress-serviceaccount --namespace ingress-space

kubectl get roles,rolebindings --namespace ingress-space



VOLUMES
kubectl get persistentvolume


controlplane $ kubectl create cm cm-3392845 --from-literal=DB_NAME=SQL3322 --from-literal=DB_HOST=sql322.mycompany.com --from-literal=DB_PORT=3306
controlplane $ kubectl create secret generic db-secret-xxdf --from-literal=DB_Host=sql01 --from-literal=DB_User=root --from-literal=DB_Passwprd=password123

kubectl get secrets db-secret-xxdf -o yaml

