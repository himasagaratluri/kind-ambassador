# kind-ambassador

* Create a kind Cluster
  Run the create-cluster.sh script to get one
  ```(shell)
  â  kind-ambassador git:(main) â source create-cluster.sh 
        Creating cluster "kind-ambassador" ...
        âĸâĄ Ensuring node image (kindest/node:v1.25.2) đŧ 
        âĸâĄą Ensuring node image (kindest/node:v1.25.2) đŧ 
        â â  Ensuring node image (kindest/node:v1.25.2) đŧ 
        â Ensuring node image (kindest/node:v1.25.2) đŧ 
        â Preparing nodes đĻ  
        â Writing configuration đ 
        â Starting control-plane đšī¸ 
        â Installing CNI đ 
        â Installing StorageClass đž 
        Set kubectl context to "kind-kind-ambassador"
        You can now use your cluster with:

        kubectl cluster-info --context kind-kind-ambassador

        Have a nice day! đ
  ```



### Deployment

![deployment-arch](img/arch.jpg "ingress-targets")

## Install metallb
* exec install-metallb.sh
* `docker network inspect -f '{{.IPAM.Config}}' kind` to grep the valid ranges for the LB
