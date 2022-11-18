# Kubernetes: working with secrets and voume mounts

- Create a new secret in the `myapp` namespace named `mysecret`. It should contain the secret `password: mypass`.
- Verify that the secret was created and is correct (decode the hash to verify).
- Mount the secret to the deployed pod at the `/etc/secret` path.
- Add a sidecar container to your `nginx` pod and have it share a volume mount path with the original container
  - Sidecar should be named `sidecar` and use the same `nginx` image
  - Sidecar should run the command `while sleep 2; do echo $(date) >> /etc/shared/hey.txt; done`
  - Configure both containers with an `emptyDir` type volume mount to the `/etc/shared` path
- Verify our shared volume mount is working and that our `echo` command results are available to pod `nginx`