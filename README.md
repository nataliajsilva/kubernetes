# kubernetes
Atividade - Matéria: Infrastructure and Cloud Computing - Turma: MBA FULL_02 FSD02

Subir dois pods, nginx e mysql, mapeando a porta 80 do nginx para acesso externo ao cluster e permitir que o contêiner do nginx tenha comunicação de rede no contêiner mysql pela porta 3306. 
A atividade pode ser feita localmente (minikube), AKS (Azure), EKS (AWS) ou no GKE (GCP). 
Se quiser criar o cluster nuvem Kubernetes com Terraform é opcional. 

# Comandos
 
#### PODS
##### $ kubectl get nodes                       -> list nodes
##### $ kubectl run ngpod --image=nginx:latest  -> run pod
##### $ kubectl get pods                        -> list pods
##### $ kubectl get pods –watch                 -> list pods
##### $ kubectl exec –it ngpod – sh             -> access pod
##### $ kubectl apply –f primeiro-pod.yaml      -> exec file
##### $ kubectl delete pod [name]               -> del pod
##### $ kubectl delete –f primeiro-pod.yaml     -> del file
##### $ kubectl run -it --image=ubuntu – bash   -> run and exec
##### $ kubectl top pod                         -> show cpu mem pods (metrics.server)

#### LOGS
##### $ kubectl get events                        -> node events
##### $ kubectl get events -n aulainfra           -> nm events
##### $ kubectl describe pod/mysql -n aulainfra   -> details pod
##### $ kubectl describe service/app -n aulainfra -> details pod
##### $ kubectl logs mysqldb-0 -n aulainfra       -> pod logs

#### DEPLOYMENT
##### $ kubectl get deployments
##### $ kubectl rollout history deployment deployment-01
##### $ kubectl apply –f [FOLDER/FILE] –record
##### $ kubectl annotate deployment deployment-01 kubernetes.io/change-cause=“texto“
##### $ kubectl rollout undo deployment deployment-01 --to-revision=1

# Links

 https://kubernetes.io/docs/tasks/tools/

 https://docs.microsoft.com/en-us/azure/aks/kubernetes-walkthrough
