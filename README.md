# MigracionKubernetes
Proyecto para migrar la web GamesInfo a Kubernetes

```bash
docker build . -t jpastorr/servidor -f Dockerfile.servidor
docker build . -t jpastorr/gamesinfo_mail -f Dockerfile.mail
docker build . -t jpastorr/gamesinfo_mysql  -f Dockerfile.mysql

kubectl create -f hazelcast_perms.yaml

helm install --name gamesinfo helm/GamesInfo
```
