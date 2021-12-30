---
marp: true
---

<!-- _class: invert -->

## Google GKE - Autopilot

Autopilot is a new mode of operation in Google Kubernetes Engine (GKE) that is
designed to reduce the operational cost of managing clusters, optimize your
clusters for production, and yield higher workload availability. The mode of
operation refers to the level of flexibility, responsibility, and control that
you have over your cluster.

---

## Google GKE - Autopilot (II)

* In addition to the benefits of a fully managed control plane and node
  automations, GKE offers two modes of operation:

  * Autopilot: GKE provisions and manages the cluster's underlying
    infrastructure, including nodes and node pools, giving you an optimized
    cluster with a hands-off experience.

  * Standard: You manage the cluster's underlying infrastructure, giving you
    node configuration flexibility.

---

## Google GKE - Autopilot (III)

* With Autopilot, you no longer have to monitor the health of your nodes or
  calculate the amount of compute capacity that your workloads require.
  Autopilot supports most Kubernetes APIs, tools, and its rich ecosystem. You
  stay within GKE without having to interact with the Compute Engine APIs, CLIs,
  or UI, as the nodes are not accessible through Compute Engine, like they are
  in Standard mode. You pay only for the CPU, memory, and storage that your Pods
  request while they are running.

---

## Google GKE - Autopilot (IV)

* Autopilot clusters are pre-configured with an optimized cluster configuration
  that is ready for production workloads. This streamlined configuration follows
  GKE best practices and recommendations for cluster and workload setup and
  security. Some of these built-in settings (detailed in the table below) are
  immutable and other optional settings can be turned on or off.

---

## Google GKE - Autopilot (V)

* Autopilot comes with a SLA that covers both the control plane and your Pods.
  With Autopilot, as the underlying infrastructure is abstracted away, you can
  focus on the Kubernetes API and your deployments. Autopilot uses the resource
  requirements that you define in your PodSpec and provisions the resources for
  the deployment such as CPU, memory, and persistent disks.

---

## Google GKE - Autopilot (VI)

* There are two main reasons why you might want to use the Standard mode of
  operation instead of Autopilot:

  * You require a higher level of control over your cluster configuration.

  * Your clusters must run workloads that do not meet Autopilot constraints.

---

<!-- _class: invert -->

## Workload Limitations And Restrictions

* Autopilot supports most workloads that run your applications. In order for GKE
  to offer management of the nodes and provide you with a more streamlined
  operational experience, there are a few restrictions and limitations when
  compared to GKE Standard. Some of these limitations are security best
  practices, while others allow Autopilot clusters to be safely managed.

* Workload limitations apply to all Pods, including those launched by
  Deployments, DaemonSets, ReplicaSets, ReplicationControllers, StatefulSets,
  Jobs, and CronJobs.
