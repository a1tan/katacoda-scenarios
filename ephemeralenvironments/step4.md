Check if applications installed and synchronized:

`kubectl get application -n argocd -owide -w`{{execute}}

Check if namespaces applied:
`kubectl get ns`{{execute}}

Wait until all applications up and running(It can take some time, but it should be done in a few minutes).
 
Note: "argocdsecretsynchronizercrds" hangs on OutOfSync state but it is working fine.