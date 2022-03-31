> Labels are key/value pairs that are attached to objects, such as pods. Labels are intended to be used to specify identifying attributes of objects that are meaningful and relevant to users, but do not directly imply semantics to the core system. Labels can be used to organize and to select subsets of objects. Labels can be attached to objects at creation time and subsequently added and modified at any time. Each object can have a set of key/value labels defined. Each Key must be unique for a given object.

#### show labels - kubectl get pods --show-labels

#### create labels - kubectl run pod(name) --image nginx --labels=env='dev  owner=harry'

#### create labels using dry run -kubectl run pod(name) --image nginx --labels='env=dev,owner=harry1' --dry-run=client -o yaml

#### to get specific envinorments labels - kubectl get pods -l env=prod

https://kubernetes.io/docs/concepts/overview/working-with-objects/labels/

## Label selectors
> Unlike names and UIDs, labels do not provide uniqueness. In general, we expect many objects to carry the same label(s).
Via a label selector, the client/user can identify a set of objects. The label selector is the core grouping primitive in Kubernetes.

The API currently supports two types of selectors: equality-based and set-based. A label selector can be made of multiple requirements which are comma-separated. In the case of multiple requirements, all must be satisfied so the comma separator acts as a logical AND (&&) operator.

The semantics of empty or non-specified selectors are dependent on the context, and API types that use selectors should document the validity and meaning of them.


# What is limits in Kubernetes?
 > Requests and limits are the mechanisms Kubernetes uses to control resources such as CPU and memory. ... If a container requests a resource, Kubernetes will only schedule it on a node that can give it that resource. Limits, on the other hand, make sure a container never goes above a certain value

 https://www.densify.com/kubernetes-tools/kubernetes-resource-limits

 https://learning.edureka.co/classroom/recording/922/8407/1492629?tab=ClassRecording
