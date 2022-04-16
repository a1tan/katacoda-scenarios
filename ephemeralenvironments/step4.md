Check if applications installed and synchronized:

`kubectl get application -n argocd -owide -w`{{execute}}

Check if namespaces applied:
`kubectl get ns`{{execute}}

Wait until all applications up and running(It can take some time, but it should be done in a few minutes). Wait specifically "sampleapp-f-ephemeralpullrequest-3" application Synced and Healty.

Note: "argocdsecretsynchronizercrds" hangs on OutOfSync state but it is working fine.