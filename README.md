# Metric-Collector
## _Collect metric data_

![Prometheus](./prometheus_logo.png)

> 이종 가상 운용 환경 대상 시스템 리소스 모니터링
> 
> 가상화 프랫폼(K8S, OpenStack, VMware ...) 단위 Metric 데이터 수집

## Features

- Prometheus의 Exporter를 통해 이종 가상 운용 서버의 리소스(CPU, Memory, GPU 등) 지표 수집
- Service discovery 메커니즘을 통한 모니터링 리소스 검색
- K8S Label Selector를 통한 모니터링 수행

## Install Node Exporter

```sh
$ cp exporter/node_exporter-1.3.1.linux-amd64/node_exporter /usr/local/bin
$ cp exporter/node_exporter-1.3.1.linux-amd64/node_exporter.service /etc/systemd/system/
$ systemctl daemon-reload
$ systemctl start node_exporter
$ systemctl status node_exporter
$ systemctl enable node_exporter
```

## Install Prometheus

```sh
$ kubectl create -f kube/prometheus.yml
```
