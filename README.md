# OpenStudio Server

[OpenStudio Server](https://github.com/NREL/OpenStudio-server) is a Kubernetes deployable instance which allows for large-scale parametric analyses of building energy models using the OpenStudio SDK in the form of OpenStudio measures.

## Introduction

This helm chart installs a OpenStudio-server instance (https://github.com/NREL/OpenStudio-server/) deployment on a [Kubernetes](http://kubernetes.io) cluster using the [Helm](https://helm.sh) package manager. 
You can interface with OpenStudio-server cluster using the [Parametric Analysis Tool](https://github.com/NREL/OpenStudio-PAT), which is part of the OpenStudio collection of software tools, or use OpenStudio CLI utility (TODO).

## Prerequisites

- Kubernetes 1.3+ cluster.  Please refer to README.md in google/README.md or aws/README.md for information on how to provision a cluster. 
- helm client
- kubectl client

## Installing the Chart

To install the chart with the release name `my-release`:

```console
$ ./scrips/install.sh
```

The command deploys Prometheus on the Kubernetes cluster in the default configuration. The [configuration](#configuration) section lists the parameters that can be configured during installation.


## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

```console
$ ./scrips/uninstall.sh
```

The command removes all the Kubernetes components associated with the chart and deletes the release.
Note - the uninstall removes nfs clients first so the do not hang.  TODO - add in pre-delete hook in helm to remove these first or explore nfs mount options that prevent deadlock. 

## Configuration

The following table lists the configurable parameters of the Prometheus chart and their default values.

Parameter | Description | Default
--------- | ----------- | -------
`TODO` | TODO | `TODO` |

Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`. For example,

```console
$ helm install ./openstudio-server --name my-release \
    --set nfs.disk.size=50GB
```




