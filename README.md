# Helm-deployment-to-Kubernetes-using-ArgoCD

A critical part of DevOps is the continuous delivery process. Following a GitOps approach Here is what I did in a recent mini-project of mine:

1. Using helm as my K8 package manager, I wrote a simple nginx server deployment and service.

2. I packaged the files into a helm chart and pushed the code base
to GitHub

3. I used GitHub pages to statically host my helm charts and thus using it as a chart repository by initializing an index.yaml file.

4. Provisioned a managed Kubernetes cluster locally using minikube.

5. Set up argocd on my Kubernetes cluster

6. Configured my argocd instance to watch for changes in my
git repository and provision the resources specified by the helm
chart onto my Kubernetes cluster.

Technologies used: #kubernetes #argocd #helm

Challenge faced:
A key feature of helm is to enable you roll out releases on your cluster and be able to rollback. I found that when I deployed helm charts 
to Kubernetes via argocd, I was unable to harness this feature as opposed to just deploying directly to Kubernetes without using argocd. Any thoughts? 
