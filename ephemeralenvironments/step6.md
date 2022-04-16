First get kubeconfig to connect vcluster environment:

`kubectl get secret vc-cluster-f-ephemeralpullrequest-3 -n cluster-f-ephemeralpullrequest-3-namespace -ojsonpath={.data.config} | base64 -d > config.yaml`{{execute}}

Replace server address to be accessed by localhost:

`sed -i 's/cluster-f-ephemeralpullrequest-3.cluster-f-ephemeralpullrequest-3-namespace.svc.cluster.local/localhost:8081/g' config.yaml`{{execute}}

Port forward to VCluster:

`kubectl port-forward svc/cluster-f-ephemeralpullrequest-3 -n cluster-f-ephemeralpullrequest-3-namespace 8081:443 &`{{execute}}

Click Ctrl + C, it will continue running at the background.

`<kbd>Ctrl</kbd>+<kbd>C</kbd>`{{execute}}

Port forward to sample app service:

`kubectl port-forward svc/sampleapp-f-ephemeralpullrequest-3 -n sampleapp-f-ephemeralpullrequest-3-namespace --kubeconfig config.yaml 8082:80 &`{{execute}}

Click Ctrl + C, it will continue running at the background.

`<kbd>Ctrl</kbd>+<kbd>C</kbd>`{{execute}}

Check the endpoint:

`curl http://localhost:8082/Sample`{{execute}}

You will see the following output:

```
<p>Hello from PR-Vcluster-Dev</p>
```
