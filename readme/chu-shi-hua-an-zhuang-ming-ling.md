# 初始化安装命令

```markdown
#初始化安装命令
kubeadm init --kubernetes-version=1.21.6  \
--apiserver-advertise-address=10.30.1.219  \
--image-repository registry.aliyuncs.com/google_containers  \
--service-cidr=10.96.0.0/16  \
--pod-network-cidr=10.244.0.0/16  \
--ignore-preflight-errors=SystemVerification  \
--upload-certs
```
