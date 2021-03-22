# K3s monitoring (Very early work) 
# To deploy
The setup assumes a RWX storage class called ```mekom-nfs```

```kubectl apply -R -f ./  ```


```kubectl get svc -n monitoring```

Should return 

```
NAME                       TYPE           CLUSTER-IP      EXTERNAL-IP    PORT(S)          AGE
alertmanager               NodePort       10.43.37.111    <none>         9093:31469/TCP   82m
grafana                    LoadBalancer   10.43.60.189    192.168.0.15   3000:31661/TCP   82m
prometheus                 LoadBalancer   10.43.214.142   192.168.0.16   9090:32461/TCP   82m
prometheus-arm-exporter    ClusterIP      None            <none>         9243/TCP         82m
prometheus-node-exporter   ClusterIP      None            <none>         9100/TCP         82m

````

access grafana at 192.168.0.15 and prometheus at 192.168.0.16

The password and username for grafana is admin/admin
