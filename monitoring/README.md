# Les dockers sont bien lancés et accessibles via le client : 
```powershell
[root@monitoring monitoring]# docker ps
CONTAINER ID   IMAGE                      COMMAND                  CREATED          STATUS          PORTS                                         NAMES
b04c5644dfab   prom/alertmanager:latest   "/bin/alertmanager -…"   25 minutes ago   Up 25 minutes   0.0.0.0:9093->9093/tcp, [::]:9093->9093/tcp   alertmanager
89765b01b2ce   grafana/grafana:latest     "/run.sh"                25 minutes ago   Up 25 minutes   0.0.0.0:3000->3000/tcp, [::]:3000->3000/tcp   grafana
6e4f5806ceb6   prom/prometheus:latest     "/bin/prometheus --c…"   25 minutes ago   Up 25 minutes   0.0.0.0:9090->9090/tcp, [::]:9090->9090/tcp   prometheus
```