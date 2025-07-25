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


```bash
#### Challenge - 2 
🟢 Challenge 2: Allow Only From Specific Pod
Allow ingress to nginx only from a pod with label role=client.

Tasks
Label your BusyBox pod:

```bash
kubectl run busybox --rm -it --image=busybox -n network-demo --labels="role=client" -- sh
```


Apply a policy to nginx that:

Denies all ingress

Allows ingress only from pods with role=client

✅ Expected: Only labeled BusyBox pod can connect to nginx.

