# Helm chart for EngineMq Broker

With this repo, you can easily install an EngineMQ broker in a helm environment under kubernetes (k8s). Simply use the ```helm install...``` command without modification or create your own **values.yaml** file and apply it with the ``` helm install -f myfile...``` command.

Quick installation as prod1:

```helm install prod1 ./```

Custom installation as prod1:

```helm install -f myvalues.yaml prod1 ./```

## What you can configure
What ports do you allow access to:
```
service:
  portMq: 16677
  enableWebUI: true
  portWebUI: 16688
```

What would you like to log:
```
log:
  logLevel: info
```

Do you want to store unsent messages:
```
persistence:
  enabled: true
  size: 8Gi
```

You want to automatically set / update resources from a github repo:
```
resourceOrigin:
  repo: Organization-Or-User/repo-name
  token: ghp_?????
  branch: master
  folder: /
```

You can find more information at https://enginemq.github.io/
