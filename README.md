### EKS PoC

Steps from https://developer.hashicorp.com/terraform/tutorials/kubernetes/eks

```
git clone https://github.com/hashicorp/learn-terraform-provision-eks-cluster
cd learn-terraform-provision-eks-cluster
aws configure
terraform init
terraform apply
aws eks --region $(terraform output -raw region) update-kubeconfig \
    --name $(terraform output -raw cluster_name)
```
