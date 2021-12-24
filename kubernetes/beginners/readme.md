# Kubernetes at first sight

## Docker basics

<img src="beginners.assets/image-20211224091640448.png" alt="image-20211224091640448" style="zoom:50%;" />

what is docker ?

simplify containers 

run natively on linux 

but run anywhere (linux,macos,windows)

 and allow to ship code with infra (how to run the code)

<img src="beginners.assets/image-20211224092542739.png" alt="image-20211224092542739" style="zoom:50%;" />

<img src="beginners.assets/image-20211224092635613.png" alt="image-20211224092635613" style="zoom:33%;" />

## Kubernetes

describe the desired state

1- pods live and die

2- service abstract pods from IP addresses and load balances between pods

3- 

<img src="beginners.assets/image-20211224101530838.png" alt="image-20211224101530838" style="zoom:50%;" />

![image-20211224103444090](beginners.assets/image-20211224103444090.png)



## Kubernetes from a developer perspective

Help to deploy, scale and manage containerized applications

key features:

* service discovery
* storage orchestration
* automate rollouts/rollbacks
* self healing
* secrets and configuration
* horizontal scaling

### Before kubernetes

we may load-balance on VirtualMachines running some docker containers.

<img src="beginners.assets/image-20211224115006315.png" alt="image-20211224115006315" style="zoom:40%;" />



These docker containers may look like the following :

<img src="beginners.assets/image-20211224115710999.png" alt="image-20211224115710999" style="zoom:50%;" />

But what happens if some containers crash or if the entire VM is down?

## What is Kubernetes

declarative: describe desired state

Inside kubernetes

* nodes : they are machines running kubernetes as a cluster
* pods: they wrap containers, they have one unique IP and can communicate with all other pods in the cluster
* services: define networking properties, allow to discover applications

<img src="beginners.assets/image-20211224121221831.png" alt="image-20211224121221831" style="zoom:50%;" />

* kubectl: use api to deploy workload with yaml manifests

on each node (machine):

* kubelet: agent on each node that will report to the control manager.

* container runtime: will allow running containers inside pods

* kube-proxy: responsible for the networking, will ensure that each pod get a unique address

Pod

<img src="beginners.assets/image-20211224123429535.png" alt="image-20211224123429535" style="zoom:33%;" />

Network

<img src="beginners.assets/image-20211224123511217.png" alt="image-20211224123511217" style="zoom:50%;" />
