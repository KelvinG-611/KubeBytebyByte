## `kubectl version`
```
~ kubectl version
Client Version: version.Info{Major:"1", Minor:"22", GitVersion:"v1.22.3", GitCommit:"c92036820499fedefec0f847e2054d824aea6cd1", GitTreeState:"clean", BuildDate:"2021-10-27T18:34:20Z", GoVersion:"go1.16.10", Compiler:"gc", Platform:"darwin/amd64"}
Server Version: version.Info{Major:"1", Minor:"22", GitVersion:"v1.22.3", GitCommit:"c92036820499fedefec0f847e2054d824aea6cd1", GitTreeState:"clean", BuildDate:"2021-10-27T18:35:25Z", GoVersion:"go1.16.9", Compiler:"gc", Platform:"linux/amd64"}
```

Major version: `1`
    Overhaul of kube functionality. Huge difference that users need to pay attention. 

Minor version: `22`
	The enhancement or improvement that don't drastically alter. 

Compatibility: client and server's version don't need to be the exact same. **One minor version  difference is allowed**


## `kubectl cluster-info`
```
kubectl cluster-info
Kubernetes control plane is running at https://192.168.64.2:8443
CoreDNS is running at https://192.168.64.2:8443/api/v1/namespaces/kube-system/services/kube-dns:dns/proxy
```


### [Kube control plan] Is Kubernetes control plane reside in a dedicated Kubernetes cluster? 

| Control Plane Setup | Description | Use Case |
|---------------------|-------------|----------|
| Self-Hosted Control Plane | The control plane components run as regular pods within the same Kubernetes cluster they manage. | Suitable for smaller or more integrated environments. |
| Dedicated Control Plane Nodes | The control plane runs on dedicated nodes, separate from nodes running application workloads. | Common in larger or production-focused environments for stability and resource isolation. |
| Managed Kubernetes Services | The control plane is managed by a cloud provider and runs on separate infrastructure, with users interacting through APIs and tools. | Ideal for users who prefer a cloud-based, managed solution (e.g., GKE, EKS, AKS). |
| High-Availability (HA) Control Plane | The control plane is replicated across multiple nodes or locations for high availability. | Essential for environments where continuous operation and fault tolerance are critical. |


### [CoreDNS]
