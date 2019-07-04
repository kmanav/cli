## tkn pipeline start

Start pipelines

### Synopsis

To start a pipeline, you will need to pass the following:

- Resources
- Parameters, at least those that have no default value

```
tkn pipeline start
```

### Examples

```
To run a Pipeline that has one git resource and no parameter.

```shell
$ tkn pipeline start --resource source=samples-git
```

To run a Pipeline that has one git resource, one image resource and
two parameters (foo and bar)

```shell
$ tkn pipeline start --resource source=samples-git \
	--resource image=my-image \
	--param foo=yay \
	--param bar=10
```
```

### Options

```
  -h, --help                    help for start
  -p, --param strings           pass the param
  -r, --resource strings        pass the resource name and ref
  -s, --serviceaccount string   pass the serviceaccount name
```

### Options inherited from parent commands

```
  -k, --kubeconfig string   kubectl config file (default: $HOME/.kube/config)
  -n, --namespace string    namespace to use (default: from $KUBECONFIG)
```

### SEE ALSO

* [tkn pipeline](tkn_pipeline.md)	 - Manage pipelines
