## virtletctl virsh

Execute a virsh command

### Synopsis


This command executes libvirt virsh command.

A VM pod name in the form @podname is translated to the
corresponding libvirt domain name. If @podname is specified,
the target k8s node name is inferred automatically based
on the information of the VM pod. In case if no @podname
is specified, the command is executed on every node
and the output for every node is prepended with a line
with the node name and corresponding Virtlet pod name.

```
virtletctl virsh [flags] virsh_command -- [virsh_command_args...]
```

### Options

```
  -h, --help          help for virsh
      --node string   the name of the target node
```

### Options inherited from parent commands

```
      --alsologtostderr                  log to standard error as well as files
      --as string                        Username to impersonate for the operation
      --as-group stringArray             Group to impersonate for the operation, this flag can be repeated to specify multiple groups.
      --certificate-authority string     Path to a cert file for the certificate authority
      --client-certificate string        Path to a client certificate file for TLS
      --client-key string                Path to a client key file for TLS
      --cluster string                   The name of the kubeconfig cluster to use
      --context string                   The name of the kubeconfig context to use
      --insecure-skip-tls-verify         If true, the server's certificate will not be checked for validity. This will make your HTTPS connections insecure
      --kubeconfig string                Path to the kubeconfig file to use for CLI requests.
      --log-backtrace-at traceLocation   when logging hits line file:N, emit a stack trace (default :0)
      --log-dir string                   If non-empty, write log files in this directory
      --logtostderr                      log to standard error instead of files
  -n, --namespace string                 If present, the namespace scope for this CLI request
      --password string                  Password for basic authentication to the API server
      --request-timeout string           The length of time to wait before giving up on a single server request. Non-zero values should contain a corresponding time unit (e.g. 1s, 2m, 3h). A value of zero means don't timeout requests. (default "0")
  -s, --server string                    The address and port of the Kubernetes API server
      --stderrthreshold severity         logs at or above this threshold go to stderr (default 2)
      --token string                     Bearer token for authentication to the API server
      --user string                      The name of the kubeconfig user to use
      --username string                  Username for basic authentication to the API server
  -v, --v Level                          log level for V logs
      --virtlet-runtime string           the name of virtlet runtime used in kubernetes.io/target-runtime annotation (default "virtlet.cloud")
      --vmodule moduleSpec               comma-separated list of pattern=N settings for file-filtered logging
```

### SEE ALSO

* [virtletctl](virtletctl.md)	 - Virtlet control tool
