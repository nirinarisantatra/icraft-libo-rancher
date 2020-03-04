# Kubernetes Nextcloud
A Nextcloud and Collabora Online Kubernetes deployment with Apache, MariaDB, HAProxy, Cron and Redis.

## Requirements
* A functional Kubernetes cluster: [Rancher](https://rancher.com/) was set up for testing this repository
* A Kubernetes storage manager: [OpenEBS](https://openebs.io/) installed via Rancher catalog
* [Kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
* Kustomize: included with the latest version of Kubectl

## Deployment
* Update `mariadb/secret.yaml` with MYSQL_PASSWORD and MYSQL_ROOT_PASSWORD (can be set to anything, must be base64 encoded) 
* Update `nextcloud/ingress.yaml` with your kubernetes domain name
* Adjust storage size in `nextcloud/pvc.yaml` to fit your needs
* Run the following command to build and deploy
```shell=
$ kubectl apply -k .
```

###### tags: `iCraft` `Documentation` `Nextcloud` `Kubernetes` `Rancher`