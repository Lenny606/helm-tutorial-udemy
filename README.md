#K8S
running with minikube locally
-minikube start --force

#Add
add from artifact hub 
- helm repo add bitnami https://charts.bitnami.com/bitnami

#install
- helm install <release-name> <chart-name> --version=<version>
- helm uninstall <release-name>
- helm install local-wp bitnami/wordpress --version=26.0.0
- helm uninstall local-wp

#cmd
- helm repo list
- helm repo update - updates locally cached repos
- helm search repo <repo>
- helm show chart <reponame/path> 
- helm show readme <reponame/path>
- helm show values <reponame/path> #gets chart values
- helm get values <releaseName> #gets versions values
- helm get values <releaseName> --all
- helm get metadata <releaseName> 

#kubectl
- kubectl get pod
- kubectl get secret
- kubectl get deploy
- kubectl get svc #services
- kubectl get pv,pvc #volumes
- kubectl logs <podname>
- kubectl describe pod <podname>
- kubectl describe secret <podname>
- kubectl expose deploy my-grafana --name=grafana-svc --type=NodePort
- kubectl delete svc grafana-svc #has to be done manually
- kubectl delete pvc <volumename> #volumes has to be done manually

get secret (get value in bytes, has parsed + decoded)
- kubectl get secret my-grafana -o jsonpath='{.data.admin-password}' | base64 -d

#minikube
- minikube service grafana-svc #show ip of service