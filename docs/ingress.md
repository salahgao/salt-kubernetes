## 部署 Traefik


```
kubectl label nodes 192.168.56.11 edgenode=true
kubectl label nodes 192.168.56.13 edgenode=true
kubectl label nodes 192.168.56.14 edgenode=true

kubectl create -f /srv/addons/ingress/
```


## Traefik Dashboard

http://192.168.56.11:8580/dashboard/

  ![架构图](https://github.com/unixhot/salt-kubernetes/blob/master/docs/ingress.png)
