# Containerization

Containerization provides a method of providing reproducible, secure (both kernel and application level) application stacks. 

Containers can be provided through various kernel implementions, including containerd, docker.io, lxc, etc. and is separated from the host operation system through methods such as using `cgroups`. 

A containerized application is not inherently more secure on the application level, however through kernel separation, compromising a container can reduce the attack surface into the host OS. 

Containers also provide a, well, contained environment for something to run in. Instead of having to, say, set up an entire build chain on the host OS (your desktop) and providing the exact steps to create that environment for anyone else trying to build the software, you can use a container to create a reproducible build environment - for example the .NET containers encourage exactly this. 

# Container Orchestration

Managing how multiple containers are deployed and kept healthy is done through orchestration. Balanced across hosts, restarted when failing, etc.

- Kubernetes
- Docker Swarm
- Rancher
