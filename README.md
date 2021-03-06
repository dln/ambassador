Ambassador [![Build Status](https://travis-ci.org/datawire/ambassador.png?branch=master)](https://travis-ci.org/datawire/ambassador) [![Docker Repository](https://quay.io/repository/datawire/ambassador/status "Docker Repository")](https://quay.io/repository/datawire/ambassador)
==========

[Ambassador](https://www.getambassador.io) is an open source Kubernetes-native API Gateway built on [Envoy](https://www.envoyproxy.io), designed for microservices. Ambassador essentially serves as an Envoy ingress controller, but with many more features.

Key features include:

* Self-service configuration, via Kubernetes annotations
* First class [gRPC and HTTP/2 support](https://www.getambassador.io/user-guide/grpc)
* Support for CORS, timeouts, weighted round robin ([canary](https://www.getambassador.io/reference/canary)), [rate limiting](https://www.getambassador.io/reference/services/rate-limit-service)
* [Istio integration](https://www.getambassador.io/user-guide/with-istio)
* [Authentication](https://www.getambassador.io/reference/services/auth-service)
* Robust TLS support, including TLS client-certificate authentication

Architecture
============

Ambassador deploys the Envoy Proxy for L7 traffic management. Configuration of Ambassador is via Kubernetes annotations. Ambassador relies on Kubernetes for scaling and resilience. For more on Ambassador's architecture and motivation, read [this blog post](https://blog.getambassador.io/building-ambassador-an-open-source-api-gateway-on-kubernetes-and-envoy-ed01ed520844).

Getting Started
===============

You can get Ambassador up and running in less than a minute by running it locally with Docker. Follow the instructions here: https://www.getambassador.io#get-started.

For production usage, Ambassador runs in Kubernetes. For a Kubernetes deployment, follow the instructions at https://www.getambassador.io/user-guide/getting-started.

If you are looking for a Kubernetes ingress controller, Ambassador provides a superset of the functionality of a typical ingress controller. (It does the traditional routing, and layers on a raft of configuration options.) This blog post covers [Kubernetes ingress](https://blog.getambassador.io/kubernetes-ingress-nodeport-load-balancers-and-ingress-controllers-6e29f1c44f2d).

You can also use Helm to install Ambassador. For more information, see the instructions in the [Helm installation documentation](https://www.getambassador.io/user-guide/helm).

Community
=========

Ambassador is an open source project, and welcomes any and all contributors. To get started:

* Join our [Slack channel](https://d6e.co/slack)
* Read the [developer guide](BUILDING.md)
* Check out the [Ambassador documentation](https://www.getambassador.io/about/why-ambassador)

If you're interested in contributing, here are some ways:

* Write a blog post for [our blog](https://blog.getambassador.io)
* Investigate an [open issue](https://github.com/datawire/ambassador/issues)
* Add [more tests](https://github.com/datawire/ambassador/tree/develop/end-to-end)
