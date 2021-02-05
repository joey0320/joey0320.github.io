---
layout: post
title:  "Container Part 2"
date:   2021-02-04T14:25:52-05:00
author: Joonho Hwangbo 
categories: Container
---
# Container Part 2 - Container Internals
![Docker](/assets/docker_logo.png)


## 1. Overview
![docker internals](/assets/DockerInternals.png)
- client : docker user, sends requests using cli
- daemon (docker engine) : responsible for image management & build, authentication, security, core networking(constructs default bridge, docker0 etc), orchestration, uses the REST API to get requests from the client
- containerd : controls the container life cycle
- runc : cli that wraps around libcontainer, interacts with the kernel to construct namespaces, cgroups etc
- shim : detaches runc from containerd(????)

