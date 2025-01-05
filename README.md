# k8s-namespaces
Building and managing namespaces for my k8s clusters

# When to Use Namespaces
 - Environment Separation: Separate resources for development, staging, and production environments within the same cluster.
 - Team/Project Isolation: Provide dedicated namespaces to teams or projects to avoid interference.
 - Resource Management: Enforce resource quotas and policies for specific namespaces.
 - Testing: Create isolated environments for testing without affecting production workloads.

# Default Namespaces
Kubernetes has a few predefined namespaces:
- default :     The default namespace where resources are created if no namespace is specified.
- kube-system: 	Contains system resources and components (e.g., kube-dns, controller manager).
- kube-public:  A namespace for public resources; generally not widely used.
- kube-node-lease:	Used for node heartbeat tracking, primarily for internal cluster operations.

# Check resources within namespace
Check all resources with the namespace using:
 $ kubectl get all -n kube-system

# Extract the yaml details from an existing namespace(or any resource)
 $ kubectl get namespace devops-tools -o yaml

 