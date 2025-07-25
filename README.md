# Kube-Prep


#### Challenge - 1

🔰 Challenge 1: Deny All Ingress to a Pod
Block all incoming traffic to an nginx pod.

Tasks
Create a namespace: network-demo

Deploy an nginx pod in it.

From a busybox pod in the same namespace, confirm access with:
```bash

wget --spider nginx
Apply a NetworkPolicy to deny all ingress to the nginx pod.

✅ Expected: BusyBox should no longer reach nginx.

#### Challenge - 2