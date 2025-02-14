### Environment Variables vs ConfigMaps

Environment Variables are set directly in a pod configuration to pass configuration data to a container. They're fixed once the container starts.

ConfigMaps are Kubernetes objects used to store configuration data separately from container images, making it easier to manage and share configurations across different containers. They can be updated independently of container images.

In practice, you can use ConfigMaps to store your configuration data and then use those data as Environment Variables in your containers. This approach combines the flexibility of ConfigMaps with the simplicity of using Environment Variables.


### Liveness Probe vs Readiness Probe

Liveness Probe: Determines if a container is running properly. If the liveness probe fails, Kubernetes will restart the container. This helps to ensure that your application recovers from problems like deadlocks or other issues that make it unresponsive.

Readiness Probe: Checks if a container is ready to handle requests. If the readiness probe fails, Kubernetes stops sending traffic to the container until it passes the probe again. This is useful for ensuring that traffic is only sent to containers that are fully started up and ready to process requests.

Both probes help manage container states to improve the reliability and availability of services in Kubernetes.

### Kubeadm vs Kubelet vs Kubectl

Kubeadm : Kubeadm is a tool for bootstrapping a Kubernetes cluster. Helps you set up and configure the cluster.

Kubelet: Kubelet is an agent that runs on each node in a Kubernetes cluster. It ensures that containers are running in a Pod. It's responsible for starting, stopping, and maintaining containers on the node. 

Kubectl: Kubectl is a command-line tool for interacting with the Kubernetes cluster.

### Services in Kubernetes

In Kubernetes, a Service is a method for exposing a network application that is running as one or more Pods in your cluster.

### Service Types

Kubernetes Service types allow you to specify what kind of Service you want.

#### 1. ClusterIP

Exposes the Service on a cluster-internal IP.

#### 2. NodePort

Exposes the Service on each Node's IP at a static port (the NodePort).

#### 3. LoadBalancer

Exposes the Service externally using an external load balancer.






