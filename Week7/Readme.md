# Kubernetes Administration in Depth
## Below are the task details:

Your organization is evolving, and your CTO wants to streamline the build and deployment process. As a DevOps engineer, you have been tasked to deploy a local docker images registry on Kubernetes to store the docker images in the namespace called “democloudops”  and should meet the following requirements:

**Cluster Provisioning:**
*  Provision a Kubernetes regional cluster with at least three worker nodes.
*  Ensure that the nodes are distributed across different availability zones.

**Sample Deployment:**
*  The Docker registry should be deployed with three replicas, and each replica should be scheduled on a separate node.
*  Pod runs in a container with image `registry:2.8.2` and name as `registry-cloudops`
*  The application container should store images under `/var/lib/10weeksofcloudops`.

**Storage:**
*  Configure a Persistent Volume (PV) to store data for the application.
*  The PV should request at least 50Gi of storage space.
*  Ensure the data stored in the PV survives pod restarts.

**Container Configuration:**
*  The application container should expose itself on port 5000.
*  Kubelet should perform health checks on the registry-cloudops and restart the pod if it doesn't respond on TCP port 5000 for 30 seconds. Kubelet should wait for 15 seconds before performing its first health check
*  The container should request 1Gi Memory, and the limit should be 2Gi

**Init Container:**
*  Implement an init container within the registry-cloudops deployment to ensure the presence of the data directory required by the Docker registry.
*  The init container should use an Alpine-based image and create the data directory "/var/lib/10weeksofcloudops" if it doesn't exist.


**Service Exposure:**
*  Create a Kubernetes load balancer service to expose the application externally.
*  The service should map an external port to port 5000 on the pods.

**Network Policies:**
*  Implement Network Policies to restrict incoming and outgoing network traffic for the Docker registry pods.
*  Allow necessary communication while enforcing security practices.


**Secrets and ConfigMap:**
*  Store sensitive information in Kubernetes Secrets, such as authentication credentials for the Docker registry.
*  Utilize a ConfigMap to manage configuration settings for the Docker registry deployment.

**Backup and Recovery:**
*  Define a backup strategy for the data stored in the Persistent Volume.
*  Explore options for restoring the registry in case of data loss or pod failures.

**Perform cluster upgrade to 1 major version**
*  After the upgrade, make sure that your cluster is healthy, including the workload

**Deliverables:**
*  Your solution should be well-structured, documented in a blog including the GitHub repo, and optimized for the best Kubernetes architecture, resource utilization, and security practices.
*  Please also tag me(piyush-sachdeva) and `#10weeksofcloudops` in the Linkedin/Twitter post so that we can track all the submissions.

*  Please provide a detailed YAML manifest or command set that demonstrates how you would achieve the above requirements.
*  Also, include any necessary explanations or considerations related to your implementation.

Note: Feel free to use any appropriate resources, such as Kubernetes documentation, to assist in your implementation. Good luck!
