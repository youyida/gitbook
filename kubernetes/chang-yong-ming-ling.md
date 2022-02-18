# 常用命令

{% code title="" %}
```markdown
#创建命令空间
kubectl create ns [namespace]

#删除namespace
kubectl delete ns [namespace]

kubectl apply -f calico.yaml
kubectl delete -f calico.yaml
kubectl get pod --all-namespaces

#查看node主机信息
kubectl get node -o wide

#添加标签
kubectl label node k8s-node1 disk=spinning

#查看标签
kubectl get nodes --show-labels

#查看日志
kubectl logs -f -n kube-system calico-node-c8ckd

#查看api
kubectl api-resources|grep rbac.authorization.k8s.io

#查看pod yaml
kubectl get pod -n orchestrator sgcc-portal-portal-service-6b6c7ddc89-9nsrn -o yaml

#删除pod
kubectl delete pod -n kube-system <pod-name>

#添加 NodePort
kubectl patch service -n argocd argocd-server -p '{"spec": {"type": "NodePort"}}'


#进入容器
kubectl exec -it -n <namespace> <pod-name> /bin/sh
#导出pod日志
kubectl logs <pod-name> -n <namespace> > log.txt
#调试
kubectl describe deployments.apps -n drone drone
#帮助
kubectl explain Deployment.spec
#复制容器内文件
kubectl cp -n <namespace> <pod-name>:/home/rpa/1720.txt /root/2
#复制宿主机文件到容器
kubectl cp swap.log orchestrator-province/sgcc-portal-portal-service-7ccbc977cb-jjhfl:/app/1

查看证书有效期
openssl x509 -enddate -noout -in 证书名
```
{% endcode %}
