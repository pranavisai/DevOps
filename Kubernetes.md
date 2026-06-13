## Kubernetes

A container orchestration technology that manages and deploys thousands of containers in a cluster.

1. Cluster: It is a set of nodes. Used so that in case one of the nodes fails, the others are available to keep the services running.
2. Cluster has a Control Plane (Master Node) and workers. 
3. The information of the cluster is stored, and the management of the nodes is done through the Control Plane.
4. The Control Plane is another node that has Kubernetes components installed in it.
5. The Kubernetes components installed are: kube-apiserver, etcd, controller-manager, and kube-scheduler.
6. kube-apiserver: acts as the frontend for Kubernetes. All outside interactions happen through this.
7. etcd: It is a distributed, reliable key-value store by Kubernetes to store all the data required to manage the cluster.
8. controller-manager: The brain behind the orchestration. Responsible for noticing and responding when the modes, containers, or endpoints go down. The controllers make decisions to bring up new containers in such cases.
9. kube-scheduler: It is responsible for distributing work or containers across multiple modes for newly created containers and assigns them to nodes.
10. On worker nodes, we have the kublet: This is the agent that runs on each node in the cluster. This agent makes sure that the containers are running on the nodes as expected.
11. On the worker nodes, we also have kube-proxy: This is responsible for maintaining the rules on the nodes. It helps in communicating with each other. The worker nodes and the containers need to communicate with each other.
12. We also have "container runtime" on the worker nodes: It is responsible for running the containers. This is important because we are running applications in the form of containers.
13. Kubernetes was originally made to support the runtime of Docker containers specifically, but over time, it evolved to support other container runtimes. It no longer supports the runtime component of Docker, which is managed by containerd.

## Kubectl
1. It is the command-line utility of Kubernetes.
2. It is the tool to operate the Kubernetes cluster. Eg: To view the status of the cluster, to provision applications, to scale up, down, delete, and so on.
# commands
1. kubectl version
2. kubectl --help
3. kubectl get nodes -> for the name and number of the nodes, the status, roles, age (how long it has been up), version of Kubernetes running on the system,
4. kubectl get nodes -o wide -> for all the ones above and extra -> internal-ip, external-ip, os-image, kernel-version, container-runtime.

## PODS
1. Kubernetes does not deploy containers directly on the worker nodes. The containers are encapsulated into a Kubernetes object known as pods.
2. A pod is a single instance of an application. It is the smallest object that can be created in Kubernetes.
3. When we want to scale up, we do not add more containers to the pods. We create more pods.

# commands
1. Example of creating a pod from an image: kubectl run podname --image=imagename
2. The images are pulled from the Docker Hub, which has the latest images of various applications. Kubernetes can be configured to pull various images from the public or private repository according to the organizations rules.
3. Checking if the pod is running? -> kubectl get pods
