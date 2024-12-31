# Talos etcd backup 

This chart is used to deploy a cronjob that will backup the etcd data to an S3 bucket.

## Example secrets

S3 credentials:
```
apiVersion: v1
kind: Secret
metadata:
  name: talos-backup-secrets
  annotations:
    kubernetes.io/service-account.name: talos-backup-secrets
data:
  AWS_ACCESS_KEY_ID: <data>
  AWS_SECRET_ACCESS_KEY: <data>
  CUSTOM_S3_ENDPOINT: <data>
```

Talosconfig: 
```
apiVersion: v1
data:
  talosconfig: <data>
kind: Secret
metadata:
  name: talosconfig
```

You can use the following command to create a new Talosconfig file:
```
talosctl config new --roles=os:etcd:backup etcd-backuper -n <node>
```


