
[ec2-user@ip-172-31-34-157 ~]$ kubectl get pods
kubectl get svc
NAME                                READY   STATUS    RESTARTS   AGE
myapp-deployment-58dbdb69b8-kcnsp   1/1     Running   0          7m30s
myapp-deployment-58dbdb69b8-n68q8   1/1     Running   0          6m41s
myapp-deployment-58dbdb69b8-p8h49   1/1     Running   0          6m41s
myapp-deployment-58dbdb69b8-xqph9   1/1     Running   0          7m30s
NAME            TYPE        CLUSTER-IP     EXTERNAL-IP   PORT(S)        AGE
kubernetes      ClusterIP   10.96.0.1      <none>        443/TCP        12m
myapp-service   NodePort    10.108.7.242   <none>        80:30080/TCP   7m21s
[ec2-user@ip-172-31-34-157 ~]$
