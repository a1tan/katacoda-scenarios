Copy and edit XXX with your PAT then execute:

`PAT=XXX`{{copy}}

Copy and edit XXX with your Github Account Name then execute:

`GITHUB_ACCOUNT=XXX`{{copy}}

Copy and edit XXX with Github Repository Name then execute:

`REPOSITORY=XXX`{{copy}}

`export GIT_TOKEN=$PAT`{{execute}}

This will install ArgoCD controllers and ApplicationSet controllers to argocd namespace.

Wait until all resources up and running(It can take some time):

`kubectl get pods -n argocd -w`{{execute}}

