# Install Tekton Dashboard in RedHat Linux Server

To Install Tekton Dashboard first we need to create a cluster. 

To create a cluster we can use Kubernetes.

First Create a Kubernetes Cluster using below steps.

For SELinux is disabling
```
setenforce 0
```
For SELinux is disabling permanently
```
sed -i --follow-symlinks 's/SELINUX=enforcing/SELINUX=disabled/g' /etc/sysconfig/selinux
```

Enable the Ports, if not enabled, by using below commands.
```
 firewall-cmd --permanent --add-port=6443/tcp
 firewall-cmd --permanent --add-port=2379-2380/tcp
 firewall-cmd --permanent --add-port=10250/tcp
 firewall-cmd --permanent --add-port=10251/tcp
 firewall-cmd --permanent --add-port=10252/tcp
 firewall-cmd --permanent --add-port=10255/tcp
 firewall-cmd --reload
 
 modprobe br_netfilter
 echo '1' > /proc/sys/net/bridge/bridge-nf-call-iptables
 

cat <<EOF > /etc/yum.repos.d/kubernetes.repo
[kubernetes]
name=Kubernetes
baseurl=https://packages.cloud.google.com/yum/repos/kubernetes-el7-x86_64
enabled=1
gpgcheck=1
repo_gpgcheck=1
gpgkey=https://packages.cloud.google.com/yum/doc/yum-key.gpg https://packages.cloud.google.com/yum/doc/rpm-package-key.gpg
EOF


yum install -y kubelet kubeadm  kubectl

systemctl restart docker && systemctl enable docker

systemctl  restart kubelet && systemctl enable kubelet
```

Note: Before executing above command need to disable swap memory by using below command
```
swapoff -a : Temporarly

sed -i '/ swap / s/^\(.*\)$/#\1/g' /etc/fstab : permanently


vi kubeadm-config.yaml

# kubeadm-config.yaml
kind: ClusterConfiguration
apiVersion: kubeadm.k8s.io/v1beta3
kubernetesVersion: v1.22.3
---
kind: KubeletConfiguration
apiVersion: kubelet.config.k8s.io/v1beta1
cgroupDriver: cgroupfs


kubeadm init --config kubeadm-config.yaml
```

Switch to tekton normal user and execute below commands
```
  mkdir -p $HOME/.kube
  sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
  sudo chown $(id -u):$(id -g) $HOME/.kube/config

kubectl apply -f "https://cloud.weave.works/k8s/net?k8s-version=$(kubectl version | base64 | tr -d '\n')"


kubectl taint node footslog1.fyre.ibm.com node-role.kubernetes.io/master:NoSchedule-

kubectl run nginx-demo --image=nginx --port=80
 
kubectl expose pod nginx-demo --port=80 --type=NodePort

kubectl apply --filename https://storage.googleapis.com/tekton-releases/pipeline/latest/release.yaml
kubectl apply --filename https://storage.googleapis.com/tekton-releases/dashboard/latest/tekton-dashboard-release.yaml

kubectl get pods --namespace tekton-pipelines --watch
```
Note: Hit CTRL+C to stop monitoring.
```
kubectl edit svc tekton-dashboard -n tekton-pipelines

type: ClusterIP --> type: NodePort
```
## Uninstalling the Dashboard on Kubernetes

The Dashboard can be uninstalled by running the following command:
```
kubectl delete --filename https://storage.googleapis.com/tekton-releases/dashboard/latest/tekton-dashboard-release.yaml
```
