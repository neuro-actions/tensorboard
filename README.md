# Tensorboard action for neuro-flow

This is a [`neuro-flow`](https://github.com/neuro-inc/neuro-flow) action launching a [Tensorboard](https://www.tensorflow.org/tensorboard/) instance.

The only required argument is a reference to a storage folder with your experiment results.

### Quick example

```
jobs:
  tensorboard:
    action: gh:neuro-actions/tensorboard@master
    args:
      volumes_results_remote: $[[ volumes.results.remote ]]
```

## Arguments

### `job_name`

Predictable subdomain name which replaces the job's ID in the full job URI. `""` by default

### Example

```
args:
	job_name: "tensorboard-job"
```

### `http_port`

HTTP port to use for Tensorboard, `"6006"` by default.

### Example

```
args:
	http_port: "6666"
```

### `http_auth`

Whether to use HTTP authentication for Tensorboard. `"True"` by default

### Example

```
args:
	http_auth: "False"
```

### `volumes_results_remote`

Reference to a volume with experiment results.

### Example

```
args:
	volumes_results_remote: $[[ volumes.results.remote ]]
```