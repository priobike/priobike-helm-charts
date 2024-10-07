# priobike-helm-charts

This is a collection of helm charts for deploying PrioBike services in a Kubernetes cluster.
The helm chart repository is hosted on GitHub pages and can be accessed at [https://priobike.github.io/priobike-helm-charts/](https://priobike.github.io/priobike-helm-charts/).

## Usage

If using more than one chart make sure to set the following values globally:
- `priobikeImageRegistry`
- `namespace`

An example deployment can be found here: [https://github.com/priobike/priobike-k8s-deployment](https://github.com/priobike/priobike-k8s-deployment)

## Naming convention

The default naming convention for Kubernetes resources is as follows:

- Helm chart name: `<service-name>`
- Deployment name: `<service-name>-deployment`
- StatefulSet name: `<service-name>-statefulset`
- Container name: `<service-name>-container`
- Service name: `<service-name>-service`
- Ingress name: `<service-name>-ingress`
- ConfigMap name: `<service-name>-config`
- Secret name: `<service-name>-secret`
- Labels:
    - `app`: `<service-name>-app`
- ...

The `<service-name>` is the name of the service that the helm chart deploys. In general, this is the name of the repository that contains the service code.
If there are multiple services in the same repository, it should be a combination of the service name and the repository name.

Those values can be overridden using the `values.yaml` file.