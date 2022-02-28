Install the ArgoCD application:

`kubectl apply -k argoapplicationsets/managementstack/argocd`{{execute}}

This will install ArgoCD controllers and ApplicationSet controllers to argocd namespace.

Wait until all resources up and running:

`kubectl get pods -n argocd -w`{{execute}}

