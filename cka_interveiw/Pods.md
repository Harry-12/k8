# Multi-Container Pod Patterns
Pods can contain multiple containers, for some excellent reasons — primarily, the fact that containers in a pod get scheduled in the same node in a multi-node cluster. This makes communication between them faster and more secure
Containers within a pod can interact with each other in various ways:
Network: Containers can access any listening ports on containers within the same pod, even if those ports are not exposed outside the pod.

## Shared Storage Volumes: 
Containers in the same pod 