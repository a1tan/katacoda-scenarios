Port forward service for the namespace environment:

`kubectl port-forward svc/sampleapp-ns-f-ephemeralpullrequest-3 -n sampleapp-ns-f-ephemeralpullrequest-3-namespace 8080:80 &`{{execute}}

Check the endpoint:

`curl http://localhost:8080/Sample`{{execute}}

You will see the following output:

```
<p>Hello from PR-Namespace-Dev</p>
```
