## **------kubernetes---------**

# **fully imperative**

kubectl create \<resource\> [config]  
kubectl delete \<resource\>  

# **imperative with config files**
kubectl create -f \<filename\>  
kubectl delete -f \<filename\>  
kubectl replace -f \<filename\>  

# **declarative with config files**
kubectl apply -f \<filename\>  
kubectl diff -f \<filename\>  
kubectl delete -f \<filename\>  

# **kubectl usage**
kubectl run nginx  
kubectl describe pod nginx  
kubectl logs nginx --container=nginx  
kubectl delete pod nginx  

kubectl expose pod nginx --type=NodePort --port=80

kubectl run -it alpine-image sh

kubectl run color-api --image=accyln/color-api:1.0.0  
kubectl run color-api --image=accyln/color-api:1.0.0 --dry-run=client -o yaml  

kubectl get pods

kubectl describe pod \<podname\>

kubectl logs \<podname\>

kubectl logs \<podname\> -p

kubectl get events

kubectl get pod \<podname\> -o wide

kubectl get services

kubectl get pod -l tier=backend -l app=color-api #label filter







## **------Helm--------**

helm create helloworld

helm install \<releaseName\> helloworld

helm upgrade \<releaseName\> helloworld

helm rollback \<releaseName\> <revisionNumber>

helm install \<releaseName\> --dry-run --debug helloworld

helm template helloworld   #template command doesnt communicate with kubernetes server to check

helm lint helloworld

helm uninstall \<releaseName\>


helm status \<releaseName\> -n \<namespace\>

helm history \<releaseName\>  #this brings revision info

helm rollback \<releaseName\> 1  #revision number

helm get manifest \<releaseName\>
