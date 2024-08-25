kind create cluster --name=gitopsfc



argocd admin initial-password -n argocd
kubectl port-forward svc/argocd-server -n argocd 8080:443
 kubectl port-forward service/goserver-service 8081:8080


 https://argoproj.github.io/cd/