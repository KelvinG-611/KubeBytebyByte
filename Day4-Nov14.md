# Topic 1. Kubernetes Node - High-level
Nodes are worker machine. It can be VM or physical computer. Node is where the actual workloads run. Each node is managed by the master, which schedules the workloads and manages their state. 

1. Node can run multiple pods. Pod is the smallest deployable units in Kubernetes, each pod represents a single instance of a running process in the cluster.

2. Components. Three parts:
	1. kubelet
	2. container runtime
	3. kube-proxy ???
5. Master-Node communication
	
 	(1) Nodes receive instructions from the master, such as start / stop pods.
	
 	(2) The master also monitors the nodes and pods to ensure they are functioning correctly.
6. Resource allocation and management.

	Kubernetes schedules pods on nodes based on resource availability, ensuring efficient use of resources across the cluster.

7. Load balancing and Fault Tolerance

	Kubernetes automatically distribute pods across nodes to balance the load and maintain high availability. If a node fails, Kubernetes can reschedule its pod to other nodes. 

8. Scaling and Replication

   	Kubernetes can automatically scale the number of pods based on demand and replicate pods across nodes for redundancy and reliability. 


QA: 
1. What is `container runtime`? 

	A software that allow your system run containers. It's responsible for pulling images from container registry, managing them, and running application inside containers. 
	
	In Kubernetes , the container runtime is responsible for starting and managing lifecycle of container as dictated by Kubernetes CP. 

2. How to check container runtime? 

`kubectl describe node minikube`

![image](https://github.com/KelvinG-LGTM/KubeBytebyByte/assets/13389755/64be6e6d-36f7-4ac3-b6d3-c6dcaeab84f6)

3. What's the difference between container runtime? 
	
	Docker offering more features and flexibility.
	containerd and CRI-O are more streamlined and optimized for specific environments like Kubernetes. 

--- 
Hands-on lab
