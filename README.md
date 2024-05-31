### Fork this repo and adapt it for your environment

Make sure you have a default block storage class. 

First, fork this repo. Update the following files that refer to your repo url:

- [kustomization.yaml](./argocd/kustomization.yaml)
- [bootstrap.yaml](./argocd/bootstrap.yaml)

Update the dnsNames for certificates with the correct ingress subdomain:

- [mq-cert-domain.yaml](./components/mq/variants/cloudprovider/odf/mq-cert-domain.yaml)

Install ArgoCD and add applications:

* Add openshift-gitops operator
* Apply the ArgoCD [bootstrap.yaml](./argocd/bootstrap.yaml) to the cluster
