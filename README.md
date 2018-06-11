## Wordpress Openshift Deployment
This wiki describes the details of deploying a LAMP application  - Wordpress in Openshift

## Stack
1. OpenShift Container Platform
2. Wordpress (PHP Application)
2. MySQL Database
3. Docker - Using S2i.

## Docker 
### Docker images
A custom docker image has been created and pushed to a PNC private docker registry , details of the Dockerfile is in this repo.
An openshift deployment will use this image to create a wordpress app in a project environment and also make the application connects to a database deployment from openshift.


## Openshift Resources
### Deployment Config
### ConfigMaps
ConfigMaps bind configuration files, command-line arguments, environment variables, port numbers, and other configuration artifacts to your Pods' containers and system components at runtime. ConfigMaps allow you to separate your configurations from your Pods and components, which helps keep your workloads portable, makes their configurations easier to change and manage, and prevents hardcoding configuration data to Pod specifications.

ConfigMaps are useful for storing and sharing non-sensitive, unencrypted configuration information.

### Secrets
Secrets are secure objects which store sensitive data, such as passwords, OAuth tokens, and SSH keys, in your clusters. Storing sensitive data in Secrets is more secure than plaintext ConfigMaps or in Pod specifications. Using Secrets gives you control over how sensitive data is used, and reduces the risk of exposing the data to unauthorized users.

When you create a Secret, you can secure it with base64-encoded username and password.

### PVC
Secrets are secure objects which store sensitive data, such as passwords, OAuth tokens, and SSH keys, in your clusters. Storing sensitive data in Secrets is more secure than plaintext ConfigMaps or in Pod specifications. Using Secrets gives you control over how sensitive data is used, and reduces the risk of exposing the data to unauthorized users.

When you create a Secret, you can secure it with base64-encoded username and password.A PersistentVolumeClaim is a request for and claim to a PersistentVolume resource. PersistentVolumeClaim objects request a specific size, access mode, and StorageClass for the PersistentVolume. If a PersistentVolume that satisfies the request exists or can be provisioned, the PersistentVolumeClaim is bound to that PersistentVolume.

### Services
After you deploy an application to your cluster using a Deployment or StatefulSet object, its Pods are automatically assigned Pod IP addresses, which can be used to communicate directly with the Pods within the cluster. To enable communication beyond the cluster, you need to expose the application to external traffic using Services.

### Routes
An OpenShift route is a way to expose a service by giving it an externally-reachable hostname.

## Deployments Config Files
1. MySQL deployment yaml file
2. Wordpress deployment yaml file

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
