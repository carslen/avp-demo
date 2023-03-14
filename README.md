# avp-demo

ArgoCD Vault Plugin Demo Repository

This repository contains a bunch of demo sources to demo function of ArgoCD Vault Plugin within Catena-X Consortia
environments:

- `app/plain-avp` uses AVP without any additional stuff
- `kustomize` used AVP in conjunction with Kustomize
- `charts/*` contains to Helm charts with configured AVP placeholders

## Charts

### avp-demo1

A very simple Helm chart, deploying 2 secrets.

### avp-demo2

The same two secrets will be deployed, plus a dependency (MariaDB) with some changes to the dependency Helm Chart
in `values.yaml`.

### avp-demo3

Same Helm chart as _avp-demo2_, but this time `values.yaml` is empty. Changes are provided in `apps/argo-helm3.yaml`
as inline Helm values. 

### avp-demo4

Once again the same Helm chart, with an empty default `values.yaml` file but simulating environment specific settings using `values-demo.yaml`.

## ArgoCD Applications

In `apps` folder ArgoCD applications definitions are provided to deploy the demo apps to your ArgoCD instance.
