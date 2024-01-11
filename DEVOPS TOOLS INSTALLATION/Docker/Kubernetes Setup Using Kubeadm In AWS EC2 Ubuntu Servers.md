Agenda: Kubernetes Setup Using Kubeadm In AWS EC2 Ubuntu Servers
=======================================================

Prerequisite:
==========

3 - Ubuntu Serves

1 - Manager  (4GB RAM , 2 Core) t2.medium

2 - Workers  (1 GB, 1 Core)     t2.micro


Note: Open Required Ports In AWS Security Groups. For now we will open All trafic.

==========COMMON FOR MASTER & SLAVES START ====

# First, login as ‘root’ user because the following set of commands need to be executed with ‘sudo’ permissions.

sudo su -

# Install Required packages and apt keys.

apt-get update -y
apt-get install -y apt-transport-https
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | apt-key add -
cat <<EOF >/etc/apt/sources.list.d/kubernetes.list
deb https://apt.kubernetes.io/ kubernetes-xenial main
EOF
apt-get update -y



#Turn Off Swap Space

swapoff -a
sed -i '/ swap / s/^\(.*\)$/#\1/g' /etc/fstab

# Install And Enable Docker

apt install docker.io -y
usermod -aG docker ubuntu
systemctl restart docker
systemctl enable docker.service


#Install kubeadm, Kubelet And Kubectl

apt-get install -y kubelet kubeadm kubectl kubernetes-cni

# Enable and start kubelet service

systemctl daemon-reload
systemctl start kubelet
systemctl enable kubelet.service

==========COMMON FOR MASTER & SLAVES END=====



===========In Master Node Start====================
# Steps Only For Kubernetes Master

# Switch to the root user.

sudo su -

# Initialize Kubernates master by executing below commond.

kubeadm init

#exit root user & exeucte as normal user

exit

mkdir -p $HOME/.kube
sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
sudo chown $(id -u):$(id -g) $HOME/.kube/config


# To verify, if kubectl is working or not, run the following command.

kubectl get pods -o wide --all-namespaces

#You will notice from the previous command, that all the pods are running except one: ‘kube-dns’. For resolving this we will install a # pod network. To install the weave pod network, run the following command:

kubectl apply -f "https://cloud.weave.works/k8s/net?k8s-version=$(kubectl version | base64 | tr -d '\n')"

kubectl get nodes

kubectl get pods --all-namespaces


# Get token

kubeadm token create --print-join-command

=========In Master Node End====================


Add Worker Machines to Kubernates Master
=========================================

Copy kubeadm join token from and execute in Worker Nodes to join to cluster



kubectl commonds has to be executed in master machine.

Check Nodes
=============

kubectl get nodes


Deploy Sample Application
==========================

kubectl run nginx-demo --image=nginx --port=80

kubectl expose deployment nginx-demo --port=80 --type=NodePort


Get Node Port details
=====================
kubectl get services
