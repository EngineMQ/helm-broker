# Helm chart for EngineMq Broker

Ezzel a repo-val könnyen tudsz telepíteni egy EngineMQ broker-t helm környezetben kubernetes (k8s) alá. Egyszerűen használd a ```helm install``` parancsot módosítás nélkül vagy hozz létre egy saját **values.yaml** fájlt és alkalmazd azt a ```helm install -f myfile``` paranccsal.

Gyors telepítés prod1 néven:

```helm install prod1 ./```

Egyéni telepítés prod1 néven:

```helm install -f myvalues.yaml prod1 ./```

## Amit állítani tudsz
Milyen portokon engeded ki az elérhetőséget:

```
service:
  portMq: 16677
  enableWebUI: true
  portWebUI: 16688
```

Mit szeretnél logolni:
```
log:
  logLevel: info
```

Szeretnéd-e tárolni a ki nem küldött üzeneteket:
```
persistence:
  enabled: true
  size: 8Gi
```

Valamilyen github repo-ból szeretnéd automatikusan állítani/frissíteni az erőforrásokat:
```
resourceOrigin:
  repo: Organization-Or-User/repo-name
  token: ghp_?????
  branch: master
  folder: /
```

Bővebb információt a https://enginemq.github.io/ oldalon találsz.
