kind create cluster --name=gitopsfc

kubectl create namespace argocd

kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

kubectl port-forward svc/argocd-server -n argocd 8080:443

argocd admin initial-password -n argocd

kubectl port-forward service/goserver-service 8081:8080

 https://argoproj.github.io/cd/