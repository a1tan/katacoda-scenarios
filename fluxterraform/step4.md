Check if flux resources installed and synchronized:

`kubectl get all -n flux-system -owide -w`{{execute}}

Check if sources for Git Repository applied:
`kubectl get GitRepository -A -owide`{{execute}}

Check if sources for Kustomization applied:
`kubectl get Kustomization -owide`{{execute}}