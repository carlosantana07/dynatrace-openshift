# ArgoCD project for Dyntrace OpenShift Monitoring

## Before you deploy

### API Tokens
Create the API Token and Data Ingest token as per [dynatrace documentation](https://docs.dynatrace.com/docs/setup-and-configuration/setup-on-k8s/installation/tokens-permissions)

You can use the template located at [dynatrace-secret-template](/dynakube-secret-template) to create the kubernetes secret

### Update values.yaml

Set the parameters for `spec.source.repoURL` of the `values.yaml` file in [dynatrace-apps](/dynatrace-apps)

Update the `spec.apiURL` of the `dynakube.yaml` in [dynakube](/dynakube)

## dynatrace-apps

The main argod application is `dynatrace-apps`, it will deploy all the required components.

## dynatrace-operator

This is the CRD for DynaKube.

## dynakube

Dynakube configures the speficic settings required.

## dynatrace-service-account

This deploys the service account required to connect an existing Active Gate to OpenShift
