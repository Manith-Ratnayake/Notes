1. Cluster
A Kubernetes cluster consists of a set of nodes (machines) that run containerized applications. It includes at least one master node and multiple worker nodes. The master node manages the cluster, and the worker nodes run the actual workloads (containers).

2. Nodes
A node is a physical or virtual machine in the Kubernetes cluster. There are two types of nodes:

Master node: Responsible for controlling and managing the cluster. It runs components like the API server, scheduler, controller manager, and etcd (a key-value store).
Worker node: These run the containers and contain components like kubelet, kube-proxy, and a container runtime (e.g., Docker, containerd).

3. Pods
A pod is the smallest and simplest unit in Kubernetes. A pod is a group of one or more containers that share the same network namespace and storage. Containers in the same pod can communicate with each other using localhost. Pods also share storage volumes, allowing for persistent data storage.

Single-container pods: Most pods have a single container.
Multi-container pods: A pod can host multiple containers, which need to work together.


4. ReplicaSets
A ReplicaSet ensures that a specified number of identical pods are running at any given time. It helps maintain high availability by automatically replacing pods if they fail or are deleted. It is often used with deployments to scale the number of pods based on traffic.


5. Deployments
A Deployment is a higher-level abstraction that manages ReplicaSets and provides declarative updates to applications. It helps in:

Rolling out updates to applications.
Scaling the number of pod replicas up or down.
Rolling back to previous versions of the application.


6. Services
A Service is an abstraction that defines a logical set of pods and a policy by which to access them. Services allow for stable networking between pods, even if the pod IPs change. There are different types of services:

ClusterIP: Exposes the service on a cluster-internal IP.
NodePort: Exposes the service on a static port on each node’s IP.
LoadBalancer: Exposes the service externally using a load balancer.
ExternalName: Maps the service to a DNS name.



7. Namespaces
Namespaces provide a way to divide cluster resources between multiple users or teams. By default, Kubernetes has the default, kube-system, and kube-public namespaces. You can create custom namespaces to organize resources and manage access control.


8. ConfigMaps and Secrets
ConfigMaps store configuration data that can be used by pods and applications running inside the cluster. They allow separation of configuration from the containerized applications.
Secrets store sensitive data like passwords, OAuth tokens, or SSH keys. Secrets are more secure than ConfigMaps because they are encoded and can be mounted as volumes or environment variables.


9. Volumes and Persistent Volumes (PV)
Volumes: A Kubernetes volume is a directory accessible to all containers in a pod, allowing them to share data. It survives pod restarts.
Persistent Volumes (PV): These are volumes that are provisioned independently of the lifecycle of a pod. They are used for storing data persistently outside the container's lifecycle. A PersistentVolumeClaim (PVC) is used to request storage resources.



10. Horizontal Pod Autoscaling (HPA)
Horizontal Pod Autoscaling automatically scales the number of pod replicas based on observed CPU or memory utilization (or custom metrics). It helps handle increased traffic and load automatically.

11. DaemonSets
A DaemonSet ensures that a specific pod is running on all (or some) nodes in a cluster. It is useful for system-level services like logging agents, monitoring agents, or network proxies that need to run on every node.

12. StatefulSets
A StatefulSet manages stateful applications. Unlike deployments, stateful sets ensure that pods maintain their identity and persistent storage across restarts. It is used for applications that require stable, unique network identifiers and persistent storage (e.g., databases).

13. Jobs and CronJobs
Job: A Job ensures that a specified number of pods successfully terminate after completing their task. It's useful for batch processing or one-time tasks.
CronJob: A CronJob runs jobs on a scheduled basis, similar to cron jobs in Unix-like systems. It is used for periodic or recurring tasks.


14. Ingress
An Ingress is an API object that manages external access to services in a cluster, typically HTTP/HTTPS. It provides HTTP routing based on hostnames or URLs, and often works with load balancers to expose services to the outside world.

15. kubectl
kubectl is the command-line tool used to interact with a Kubernetes cluster. It allows users to manage resources, deploy applications, view logs, and execute commands in containers.

16. Helm
Helm is a package manager for Kubernetes. It helps in defining, installing, and upgrading applications (called charts) in Kubernetes. Helm simplifies the deployment of complex applications by managing configurations, dependencies, and releases.

17. Controller
A controller is a control loop that watches the state of the cluster and makes changes to bring the current state closer to the desired state. Examples include:

ReplicationController: Ensures a specified number of pod replicas are running.
Deployment Controller: Manages deployments and rollouts.