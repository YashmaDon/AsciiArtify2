# MVP argument
To prepare a Proof of Concept (PoC) for deploying the GitOps system on recommended Kubernetes variant. The ArgoCD product is offered.
We will choose the "one application - one cluster" approach, that is, one separate cluster will be taken for each application. For this purpose, we will use "single host kubernetes cluster" And we will choose ArgoCD as the Delivery and Deploy system for the test environment.
https://argo-cd.readthedocs.io/en/stable/assets/argocd_architecture.png

## Demo AgroCD 
If you make changes to the repository, the called sync process will get the latest version of the git repository and compare it to the current state. In the demonstrated example, you can see that the service type for ambassador has changed from NodePort to LoadBalancer and the Kubernetes manifest has been updated accordingly

![Image](./DemoArgoMVP.gif)

ArgoCD implements a GitOps approach using the Git repository as the source of truth to determine the desired state of the application. Kubernetes manifests can be specified in several ways.
## Kubernetes controller
ArgoCD is a Kubernetes controller that continuously monitors running applications and compares the current state with the desired state. A deployment whose current state differs from the target is considered out of sync. ArgoCD informs and visualizes the differences, providing opportunities for automatic or manual synchronization of the desired state.
## AgroCD install
![Image](./DemoAgroCD_CLI)