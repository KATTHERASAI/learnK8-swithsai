
# Master Kubernetes starting from scratch.

We are here to learn Kubernetes from the scratch

## Why Kubernetes ?

As we all know, Docker is used to run containers.Then why Kubernetes?
i) Single host
ii) Containers are ephemerial(short lived) in nature.
iii) Containers do not support auto scaling
iv) Containers do not support auto Healing
v) Containers do support Enterprise level features (eg: Load banlancing, firewall, api gate ways, white listing , black listing e.t.c )

Hence, Kubernetes solves the above problems.
 
## Let's understand the Kubernetes architecture

Kubernetes is by default installed as cluster

Kubernetes cluster consists of two planes: 1) Control Plane 2) Data Plane

![image](https://github.com/user-attachments/assets/e3e01ac4-31d8-4598-bc8e-02e8237fac13)


Control Plane consists of:
a) **API Server**: It is the heart of Kubernetes, where it exposes the external world to your Kubernetes cluster. It handles all incoming security requests. It does everything in Kubernetes; for example, when a user creates a pod, it will take care of which pod goes to which node, etc. It is present in the master/control plane.

b) **Scheduler**: It is responsible for scheduling your pods or resources.

c)** etcd**: Entire Kubernetes cluster information is stored as key-value pairs/objects. It acts as a backup service.

d) **Controller Manage**r: It is used to check if the controllers are up and running.

e) **Cloud Controller Manager**: In simple words, it acts as a bridge between Kubernetes and cloud providers (e.g., Amazon Elastic Kubernetes Service (EKS), Azure Kubernetes Service (AKS), etc.).

Data Plane consists of:
a) **Kubelet**: It is responsible for the creation of pods. If any pod goes down, it immediately informs the worker node and rolls out new pods.

b) **Kube-prox**y: It is responsible for networking, such as generating the IP address for pods and updating the IP tables.

c) **Docker Runtime**: It is responsible for running your container inside the pods.

**Pod**: in simple words it is the defination of how to run a container.
![image](https://github.com/user-attachments/assets/5c4a1c8b-5661-44f0-ab24-ead188ccc2ad)





