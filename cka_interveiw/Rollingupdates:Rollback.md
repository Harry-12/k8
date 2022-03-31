## What is rolling update deployment?
Updating an application

> Rolling updates allow Deployments' update to take place with zero downtime by incrementally updating Pods instances with new ones. The new Pods will be scheduled on Nodes with available resources. ... This is a requirement for performing updates without affecting application availability.

Rolling updates allow the following actions:

Promote an application from one environment to another (via container image updates)
Rollback to previous versions
Continuous Integration and Continuous Delivery of applications with zero downtime
https://kubernetes.io/docs/tutorials/kubernetes-basics/update/update-intro/

## Perform a Rolling Update on a DaemonSet

https://kubernetes.io/docs/tasks/manage-daemon/update-daemon-set/


https://github.com/lerndevops/educka/blob/master/controllers/rolling-update.md

# Rollingback 

Rollback Deployment means, going back to the previous instance of the deployment if there is some issue with the current deployment.

https://octopus.com/blog/rolling-back-kubernetes-deployment


## Perform a Rollback on a DaemonSet
https://kubernetes.io/docs/tasks/manage-daemon/rollback-daemon-set/

