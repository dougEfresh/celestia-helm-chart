# celestia node for k8s

## TL;DR

### Node Type & Network

[light-node](https://docs.celestia.org/nodes/light-node)

```yaml
nodeType: light    # full, bridge
p2pNetwork: mocha  # celestia, arabica
```

### Volume

```yaml
persistence:
  enabled: true
  existingClaim: "" # or put an existing volume claim 
```

### ConfigMap

Use existing config map for config.yaml

```yaml
celestia:
  existingConfigmap: "celestia-custom-config"
```


```yaml
apiVersion: v1
kind: ConfigMap
metadata:
  name: celestia-custom-config
  labels:
    app.kubernetes.io/component: crypto
data:
  config.toml: |
    [Node]
    StartupTimeout = "20s"
    ShutdownTimeout = "20s"
    ... 
```

---

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
