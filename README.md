# Helm chart for Global rate limit envoy service

[![Latest Version](https://img.shields.io/github/release/softonic/go-ratelimit-chart.svg)](https://github.com/softonic/go-ratelimit-chart/releases)
[![Software License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](LICENSE)
[![Average time to resolve an issue](http://isitmaintained.com/badge/resolution/softonic/go-ratelimit-chart.svg)](http://isitmaintained.com/project/softonic/go-ratelimit-chart "Average time to resolve an issue")
![GitHub issues](https://img.shields.io/github/issues-raw/softonic/go-ratelimit-chart)


# Overview

With this chart you will be able to deploy the [Rate Limit Service](https://github.com/envoyproxy/ratelimit) in a k8s cluster via helm.

# Motivation

The first thing we notice when looking at how rate limit works within Envoy is that Envoy expects you to define a Rate Limit Service. This is because Envoy by itself has no mechanism to tell if a request should be let through, or rate limited. To make things even better, Lyft recently released their version of a service that responds to this interface: [Rate limit](https://github.com/lyft/ratelimit)

For more insights of envoy rate limit architecture, [Global rate limit Envoy](https://www.envoyproxy.io/docs/envoy/v1.13.0/intro/arch_overview/other_features/global_rate_limiting).

# Quick Start

```bash
NAME_OF_RELEASE="ratelimiter"
helm install --repo https://charts.softonic.io ${NAME_OF_RELEASE} go-ratelimit
```
