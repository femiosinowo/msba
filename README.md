## Wordpress Openshift Deployment
## Stack
1. OpenShift
2. Wordpress
2. PHP/MySQL
3. Docker

## Openshift Resources
### Deployment Config
### ConfigMaps
### Secrets
### PVC
### Services
### Routes

## Deployments Config Files
1. MySQL yaml file
2. Wordpress yaml file

## Usage
### Create a Project in openshift
```
oc new-project project-name

```
### Apply yaml files
```
oc create -f mysql-deployment.yaml
oc create -f wordpress-deployment.yaml

```
This will create all resources in openshift.

##
