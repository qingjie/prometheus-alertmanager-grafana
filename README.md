
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
```
docker pull prom/prometheus
cd /opt
ls
sudo mkdir prometheus
cd prometheus
touch prometheus.yml
```
### this is for prometheus
set expandtab in vi
```
[root@ip-172-31-41-120 prometheus]# cat prometheus.yml
global:
    scrape_interval: 30s

scrape_configs:
  - job_name: 'node'
    static_configs:
     - targets: ['172.31.21.46:9100']

```

```
sudo cp /tmp/a prometheus.yml
```
### this is for node
```

```
