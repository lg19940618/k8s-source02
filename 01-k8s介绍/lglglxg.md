       1.k8s有几个组件

```
控制面:
kube-apiserver,etcd,kubec-scheduler,kube-controller-manager,cloud-controller-manager
node:
kubelet,kube-proxy,container-runtime
```

2.写下创建pod的yaml
来自官方文档:

```
apiVersion: v1
kind: Pod
metadata:
  name: nginx
spec:
  containers:
  - name: nginx
    image: nginx:1.14.2
    ports:
    - containerPort: 80
```

3.说下select有什么作用

```
前提创建资源的时候需要打标签label
通过selector可以让对象匹配对应标签，比如创建serivce的时候可以指定对应标签的pod对象
```

