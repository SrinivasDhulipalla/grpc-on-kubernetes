## Setup

* Cluster
  * Digital Ocean Managed Kubernetes
  * Modern version of Kubernetes
* Laptop
  * Left
    * Terminal
    * Chrome
  * Right
    * IntelliJ

## Outline

1. API Definition
   1. [Code Reference](api/v1/v1.proto)
   1. Resources
      * [Protocol Buffers](https://developers.google.com/protocol-buffers)
1. Code Generation
   1. [Code Reference](api/v1/v1.go)
1. gRPC Server
   1. [Code Reference](internal/server/command.go)
   1. Health API
   1. Resources
      * [Health example](https://github.com/grpc/grpc-go/tree/master/examples/features/health)
1. gRPC Client
   1. [Code Reference](internal/client/command.go)
   1. Load Balancing Policy
   1. Health API
   1. Resources
      * [Load balancing example](https://github.com/grpc/grpc-go/tree/master/examples/features/load_balancing)
      * [Health example](https://github.com/grpc/grpc-go/tree/master/examples/features/health)
1. gRPC Targets
   1. `[resolver]://[resolver-address:resolver-port]/[service-name][:service-port]`
   1. Resources
      * [gRPC Name Resolution](https://github.com/grpc/grpc/blob/master/doc/naming.md)
      * [grpc-go DNS](https://github.com/grpc/grpc-go/blob/master/internal/resolver/dns/dns_resolver.go)
1. Dockerfile
   1. [Code Reference](Dockerfile)
   1. Resources
      * [grpc-health-probe](https://github.com/grpc-ecosystem/grpc-health-probe)   
1. Kubernetes Deployment
   1. [Code Reference](k8s/01-gok-server-deployment)
1. Kubernetes Services
   1. [Code Reference](k8s/02-gok-server-services)
1. Clients in action
   1. cluster-ip
      * [Code Reference](k8s/03-gok-client-clusterip)
   1. headless
      * [Code Reference](k8s/04-gok-client-headless)
   1. load balancer
      * [Code Reference](k8s/05-gok-client-lb)
