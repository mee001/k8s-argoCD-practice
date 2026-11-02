# GitOps with ArgoCD - Working Setup

Repo: https://github.com/mee001/k8s-argoCD-practice
Path: argocd-practice/manifests
Namespace: test
Private Image: dockmee001/my-private-app:v1

Steps to restore:
1. kubectl create ns test
2. create docker secret my-registry-secret
3. kubectl apply -f argocd-practice/apps/argodeploy.yaml
4. port-forward argocd: kubectl port-forward svc/argocd-server -n argocd 8081:443
5. Open https://localhost:8081

GitOps test: change replicas -> git push -> ArgoCD auto syncs
