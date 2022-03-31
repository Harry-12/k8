can be given the same mounted storage volumes, which allows them to interact with the same files.

SharedProcessNamespace: ProcessnamespacesharingcanbeenabledbysettingshareProcessNamespace true in the pod spec. This allows containers within the pod to interact with, and signal, one an-other’s processes.

> Sidecar:   
Sidecars derive their name from motorcycle sidecars. While your motorcycle can work fine without the sidecar, having one enhances or extends the functionality of your bike, by giving it an extra seat. Similarly, in Kubernetes, a sidecar pattern is used to enhance or extend the existing functionality of the container.

Your container works perfectly well without the sidecar, but with it, it can perform some extra functions.

so, a sidecar container enhances the main container in some way, adding functionality to it.

Some examples of sidecar

using a sidecar for monitoring and logging and adding an agent for these purposes

a sidecar periodically syncs files in a webserver container’s file system from a Git repository.



> Ambassador:  
The ambassador pattern derives its name from an Ambassador, who is an envoy and a person a country chooses to represent their country and connect with the rest of the world. Similarly, in the Kubernetes perspective, an Ambassador pattern implements a proxy to the external world. Lets look at an example — If you build an application that needs to connect with a database server, the server configuration, etc, changes with the environment.

Now, the official recommendation to handle these is to use Config Maps, but what if you have legacy code that is already using another way of connecting to the database. Maybe, a properties file, or even worse, a hardcoded set of values. What if you want to communicate with localhost, and you can leave the rest to the admin? You can use the Ambassador pattern for these kinds of scenarios.

So, what we can do is create another container that can act as a TCP Proxy to the database, and you can connect to the proxy via localhost. The sysadmin can then use config maps and secrets with the proxy container to inject the correct connection and auth information.

Some examples of amsbassdor

An haproxy ambassador container receives network traffic and forwards it to the main container.

An ambassador container listens on a custom port, and forwards the traffic to the main container’s hard-coded port.



> Adapter:    
The Adapter is another pattern that you can implement with multiple containers. The adapter pattern helps you standardise something heterogeneous in nature. For example, you’re running multiple applications within separate containers, but every application has a different way of outputting log files.

Now, you have a centralised logging system that accepts logs in a particular format only. What can you do in such a situation? Well, you can either change the source code of each application to output a standard log format or use an adapter to standardise the logs before sending it to your central server. That’s where the adapter pattern comes in.

so, an adapter container transforms the output of the main container.

Some great examples of adapter

An adapter container reads log output from the main container and transforms it.

https://github.com/lerndevops/educka/tree/master/pods/multi