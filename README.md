# Helm chart for Global rate limit envoy service

[![Latest Version](https://img.shields.io/github/release/envoyproxy/ratelimit.svg)](https://github.com/envoyproxy/ratelimit/releases)
[![Software License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](LICENSE)
[![Average time to resolve an issue](http://isitmaintained.com/badge/resolution/softonic/kube-gcp-disks-roomba.svg)](http://isitmaintained.com/project/envoyproxy/ratelimit "Average time to resolve an issue")

# Overview

With this chart you will be able to deploy the [Rate Limit Service](https://github.com/envoyproxy/ratelimit) in a k8s cluster via helm.

# Motivation

The first thing we notice when looking at how rate limit works within Envoy is that Envoy expects you to define a Rate Limit Service. This is because Envoy by itself has no mechanism to tell if a request should be let through, or rate limited. To make things even better, Lyft recently released their version of a service that responds to this interface: [Rate limit](https://github.com/lyft/ratelimit)

For more insights of envoy rate limit architecture, [Global rate limit Envoy](https://www.envoyproxy.io/docs/envoy/v1.13.0/intro/arch_overview/other_features/global_rate_limiting).

# Quick Start

```bash
helm repo add softonic https://charts.softonic.io
helm install redis-sharded softonic/go-ratelimit-chart
```
