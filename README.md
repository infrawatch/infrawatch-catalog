# infrawatch-catalog

InfraWatch Catalog Index and Database. Contains the database containing the
CatalogSource of bundles for InfraWatch.

## Creating a new release

Use `opm` to update the current index and write the contents to the local
repository. This is what you'll check into git and tag for a release of STF.

```
opm index add --bundles quay.io/infrawatch-operators/smart-gateway-operator-bundle:v2.0.1 --generate
```

## Create new release from previous index

Note that all bundles and index images need to be pushed to the remote
repository.

```
opm index add \
  --bundles quay.io/infrawatch-operators/smart-gateway-operator-bundles:v2.1.0 \
  --from-index quay.io/infrawatch-operators/infrawatch-catalog:latest \
  --tag quay.io/infrawatch-operators/infrawatch-catalog:latest
```
