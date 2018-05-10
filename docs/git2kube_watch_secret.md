## git2kube watch secret

Runs watcher that periodically check the provided repository and updates K8s Secret accordingly

### Synopsis

Runs watcher that periodically check the provided repository and updates K8s Secret accordingly

```
git2kube watch secret [flags]
```

### Options

```
      --annotation strings   annotation to add to K8s Secret (format NAME=VALUE)
  -h, --help                 help for secret
  -k, --kubeconfig           true if locally stored ~/.kube/config should be used, InCluster config will be used if false (options: true|false) (default: false)
      --label strings        label to add to K8s Secret (format NAME=VALUE)
      --merge-type string    how to merge Secret data whether to also delete missing values or just upsert new (options: delete|upsert) (default "delete")
  -n, --namespace string     target namespace for the resulting ConfigMap (default "default")
  -s, --secret string        name for the resulting Secret
```

### Options inherited from parent commands

```
  -b, --branch string         branch name to pull (default "master")
  -c, --cache-folder string   destination on filesystem where cache of repository will be stored (default "/tmp/git2kube/data/")
      --exclude strings       regex that if is a match excludes the file from the upload, example: '*.yaml' or 'folder/*' if you want to match a folder (default [^\..*])
  -g, --git string            git repository address, either http(s) or ssh protocol has to be specified
      --include strings       regex that if is a match includes the file in the upload, example: '*.yaml' or 'folder/*' if you want to match a folder (default [.*])
  -i, --interval int          interval in seconds in which to try refreshing ConfigMap from git (default 10)
  -l, --log-level string      command log level (options: [panic fatal error warning info debug]) (default "info")
```

### SEE ALSO

* [git2kube watch](git2kube_watch.md)	 - Runs watcher that periodically check the provided repository
