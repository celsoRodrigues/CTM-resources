# CTM-resources
CTM resources, here is where we maintain kubernetes resources such as system operators or controllers


The project is composed by 3 repos:<br/>
- CTM-infra<br/>
- CTM-Resources<br/>
- CTM-application<br/>
    

This repo is repo should only be built after the CTM-infra as this depends on kubectl configuration to contact the server:<br/>

- Build:
1. Clone the project clone 
```
   $ git clone git@github.com:celsoRodrigues/CTM-resources.git
```
2. In the project folder build with the following commands:<br />
```
   $ kubectl -f ingressController.yaml
```
5. Check if ingress is present:<br/>
```
  $ kubectl get ing
```
 You should also have a network loadbalancer and several pods in the ingress-nginx namespace

6. This ingress controller has to be deleted before destroying the terraform infrastructure
