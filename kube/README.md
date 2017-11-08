# PromLTS kubernetes test setup.

This directory contains scripts and k8s resource definitions for PromLTS. This allows to test is locally, 
as well as on external clusters.

## Local mini-kube

To run minikube with Prometheus:

`bash ./kube/run-local.sh -i -d none` for linux or `bash ./kube/run-local.sh -i -d <vm-driver>` with some vm driver for MacOS. You can find list 
of drivers [here](https://github.com/kubernetes/minikube/blob/master/docs/drivers.md). This command will 
  - run minikube
  - setup kubectl and local custom kube/config
  - deploy local Prometheus which will be exposed on 10.0.0.88:9090 accessible from you local machine.
  
To use cluster from your terminal do:
`source ./kube/envs.sh`

From now on you can use `kubectl` as well as `minikube` command, including `minikube stop` to stop the whole cluster.
  

 