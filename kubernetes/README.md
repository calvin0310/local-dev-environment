# 1. Install kind
https://kind.sigs.k8s.io/docs/user/quick-start/

# 2. Configuration
```yaml
kind: Cluster
apiVersion: kind.x-k8s.io/v1alpha4
nodes:
- role: control-plane
- role: worker
- role: worker
- role: worker
```

# 3. Create a cluster
> kind-config.yaml is which you wrote in step 2.

```shell
kind create cluster --name local-dev --config kind-config.yaml --image kindest/node:v1.31.0
```

# 4. Check the cluster
```shell
kind get clusters
```

# 5. Delete the cluster
```shell
kind delete clusters local-dev
```