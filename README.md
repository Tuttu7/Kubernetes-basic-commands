#### To get the number of nodes in cluster

```
kubectl get nodes
```
#### To get kubernetes version

```
kubectl version
```
#### To create a new pod with the nginx image 

```
root@controlplane:~# kubectl run ngnix --image=ngnix
pod/ngnix created
```

#### To get the number of pods 

```
root@controlplane:~# kubectl get pods               
NAME    READY   STATUS         RESTARTS   AGE
ngnix   0/1     ErrImagePull   0          10s
```
#### To Find the image used to create the new pods

```
  root@controlplane:~# kubectl describe pod newpods-spbdp
```

#### To find which node the pod is sitauted :

```
kubectl describe pod newpods-k6bgs | grep -i node
Node:         controlplane/172.17.0.63
Node-Selectors:              <none>
Tolerations:                 node.kubernetes.io/not-ready:NoExecute op=Exists for 300s
                             node.kubernetes.io/unreachable:NoExecute op=Exists for 300s
```

#### To Delete the pod 

```
root@controlplane:~# kubectl delete pod webapp
pod "webapp" deleted
```

#### To change the image on this pod to redis

```
root@controlplane:~# kubectl edit pod redis
pod/redis edited
```

                             
                             

