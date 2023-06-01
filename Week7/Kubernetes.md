# Kubernetes
Kubernetes helps orchestrate and automate tasks associated with containers — an essential need as you scale. Here’s a deep dive for IT leaders on what Kubernetes can do, key terms, best practices, trends for 2023, and more.

# What is Kubernetes?
What is Kubernetes and what does it have to do with containers? Where did this unusual word come from? The agreed-upon origin is from the Greek, meaning “helmsman” or “sailing master.”

# What is Kubernetes used for?
Containers appeal to organizations for a broad range of workloads. But provisioning and operationalizing containers at scale, often in concert with microservices, is not for weekend enthusiasts. Especially for stateful apps (such as databases), it requires planning, and most experts say an orchestration tool is a must. That’s where Kubernetes comes in.

Containers, in concert with Kubernetes, are helping enterprises better manage workloads and reduce risks. In organizations using DevOps practices — including short development sprints, experimentation, and iteration — containers can be key to the evolution of processes, and to an organization’s increasing usage of cloud infrastructure and microservices.

# Why you need Kubernetes and what it can do
Containers are a good way to bundle and run your applications. In a production environment, you need to manage the containers that run the applications and ensure that there is no downtime. For example, if a container goes down, another container needs to start. Wouldn’t it be easier if this behavior was handled by a system?

That’s how Kubernetes comes to the rescue! Kubernetes provides you with a framework to run distributed systems resiliently. It takes care of scaling and failover for your application, provides deployment patterns, and more. For example: Kubernetes can easily manage a canary deployment for your system.

# Kubernetes provides you with:

Service discovery and load balancing Kubernetes can expose a container using the DNS name or using their own IP address. If traffic to a container is high, Kubernetes is able to load balance and distribute the network traffic so that the deployment is stable.
Storage orchestration Kubernetes allows you to automatically mount a storage system of your choice, such as local storages, public cloud providers, and more.
Automated rollouts and rollbacks You can describe the desired state for your deployed containers using Kubernetes, and it can change the actual state to the desired state at a controlled rate. For example, you can automate Kubernetes to create new containers for your deployment, remove existing containers and adopt all their resources to the new container.
Automatic bin packing You provide Kubernetes with a cluster of nodes that it can use to run containerized tasks. You tell Kubernetes how much CPU and memory (RAM) each container needs. Kubernetes can fit containers onto your nodes to make the best use of your resources.
Self-healing Kubernetes restarts containers that fail, replaces containers, kills containers that don’t respond to your user-defined health check, and doesn’t advertise them to clients until they are ready to serve.
Secret and configuration management Kubernetes lets you store and manage sensitive information, such as passwords, OAuth tokens, and SSH keys. You can deploy and update secrets and application configuration without rebuilding your container images, and without exposing secrets in your stack configuration.
Why use Kubernetes and containers?
Maybe you’re trying to help people in your organization understand why Kubernetes — and orchestration tools in general — are necessary in the first place.

Kubernetes lets you schedule and run containers on clusters of physical or virtual machines while automating many operational tasks. In other words, Kubernetes helps enterprises tap into the potential of containers in day-to-day work, in an automated fashion. It also helps with load balancing and ensuring high-availability environments.

Many organizations find the Kubernetes platform becomes essential when you start deploying containers in significant numbers, especially in production environments.

Thus the many marketplace statistical signals indicating growing adoption. “As more and more organizations continue to expand on their usage of containerized software, Kubernetes will increasingly become the de facto deployment and orchestration target moving forward,” says Josh Komoroske, senior DevOps engineer at StackRox.

# What Kubernetes does
The power of the open source cloud-native ecosystem comes from the breadth of complementary projects that come together around Kubernetes.

Kubernetes is an important piece of the cloud-native puzzle, but it’s important to understand that its broader ecosystem provides even more value to IT organizations.

As Red Hat’s Haff notes, “The power of the open source cloud-native ecosystem comes only in part from individual projects such as Kubernetes. It derives, perhaps even more, from the breadth of complementary projects that come together to create a true cloud-native platform.”

This includes service meshes like Istio, monitoring tools like Prometheus, command-line tools like Podman, distributed tracing from the likes of Jaeger and Kiali, enterprise registries like Quay, and inspection utilities like Skopeo, says Haff. And, of course, Linux, which is the foundation for the containers orchestrated by Kubernetes.

Choosing from and integrating a variety of tools yourself takes time, of course, which is one place where enterprise open source platforms such as Red Hat OpenShift come into play.

#  [ Read also: OpenShift and Kubernetes: What’s the difference? ]

Kubernetes eases the burden of configuring, deploying, managing, and monitoring even the largest-scale containerized applications.

In many organizations, the first step toward Kubernetes adoption to date might be best described as Oh, we can use Kubernetes for this! That means, for example, that a team running a growing number of containers in production might quickly see the need for orchestration to manage it all.

StackRox’s Komoroske expects another adoption trend to continue in the future: We can build this for Kubernetes! It’s the software equivalent of a cart-and-horse situation: Instead of having an after-the-fact revelation that Kubernetes would be a good fit for managing a particular service, more organizations will develop software specifically with Kubernetes in mind. Some people will call this “Kubernetes-native” software.
