# Kubernetes: troubleshooting a pod

- Get the amount of nodes plus their status.

```
# navigate to the terminal and run:
abc@f59afbcba41c:~/workspace$ kubectl get nodes
NAME                                         STATUS   ROLES                  AGE   VERSION
ip-172-31-15-44.us-west-2.compute.internal   Ready    control-plane,master   94s   v1.25.3+k3s1
```

> Note: **k** is preconfigured for use in place of **kubectl**

- Create the namespace `question1` and deploy `pod.yaml` to that namespace.
- Check the status of the pod and fix any issues.
- Expose this nginx pod so we can all navigate to it via the URL of this instance and a custom port.
  - Start with figuring out the best way to expose the service.