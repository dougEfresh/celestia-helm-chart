# celestia

celestia node

## TL;DR

## Introduction

```console
helm  install celestia-mocha-light celestia-node --repo https://dougefresh.github.io/celestia-helm-chart
```

## Prerequisites

## Installing the Chart

To install the chart with the release name `my-release`:

```console
helm install my-release 
```


The command deploys celestia on the Kubernetes cluster in the default configuration. The [Parameters](#parameters) section lists the parameters that can be configured during installation.

> **Tip**: List all releases using `helm list`

## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

```console
helm delete my-release
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

## Parameters

## Configuration and installation details

```yaml
nodeType: light
p2pNetwork: mocha
```