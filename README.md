
```
ssh-add centos-test.pem
ssh centos@ip
```
### https://docs.docker.com/install/linux/docker-ce/centos/

```
sudo yum install -y yum-utils \
  device-mapper-persistent-data \
  lvm2
```

```
sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo

```
```
sudo yum install docker-ce docker-ce-cli containerd.io
sudo systemctl start docker
sudo usermod -a -G docker centos
docker ps
```


