# Kubernetes at first sight

## Docker basics

<img src="learn.assets/image-20211224091640448.png" alt="image-20211224091640448" style="zoom:50%;" />

what is docker ?

simplify containers 

run natively on linux 

but run anywhere (linux,macos,windows)

 and allow to ship code with infra (how to run the code)

<img src="learn.assets/image-20211224092542739.png" alt="image-20211224092542739" style="zoom:50%;" />

<img src="learn.assets/image-20211224092635613.png" alt="image-20211224092635613" style="zoom:33%;" />

## Kubernetes

describe desired state

1- pods live and die

2- service abstract pods from IP addresses and load balances between pods

3- 

<img src="learn.assets/image-20211224101530838.png" alt="image-20211224101530838" style="zoom:50%;" />

![image-20211224103444090](learn.assets/image-20211224103444090.png)



## Kubernetes from a developer perspective

Help to deploy, scale and manage containerized applications

key features:

* service discovery
* storage orchestration
* automate rollouts/rollboacks
* self healing
* secrets and configuration
* horizontal scaling

### Before kubernetes

we may loadbalance on VirtualMachines running some docker containers.

<img src="learn.assets/image-20211224115006315.png" alt="image-20211224115006315" style="zoom:40%;" />



These docker containers may look like the following :

<img src="learn.assets/image-20211224115710999.png" alt="image-20211224115710999" style="zoom:50%;" />

But what happens if some containers crashes or if entire VM is down ?

## What is kubernetes

declarative: describe desired state

Inside kubernetes

* nodes : they are machines running kubernetes as a cluster
* pods: they wrap containers, they have one unique IP and can communicate with all other pods in the cluster
* services: define networking properties, allow to discover applications

<img src="learn.assets/image-20211224121221831.png" alt="image-20211224121221831" style="zoom:50%;" />

* kubectl: use api to deploy workload with yaml manifests

on each node (machine):

* kubelet: agent on each nodes that will report to the control manager.

* container runtime: will allow to run containers inside pods

* kube-proxy: responsible for the networking, will ensure that each pod get a unique address
