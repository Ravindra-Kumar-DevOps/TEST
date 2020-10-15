# TEST

# IXIGO TASK

1.Create a Highly available Kubernetes cluster on AWS. Do not create a Kubernetes hosted solution (like EKS). (AWS free tier should suffice for this exercise). Use Kubeadm(preferred)/kubespray/kops. If possible share a script/code which can be used to create the cluster. 

On Master Node : 10.0.1.82

[root@ip-10-0-1-82 ec2-user]# history 
    1  hostname -I
    2  vim /etc/hosts
    3  vim /etc/hosts
    4  vim /etc/hosts
    5  ping 10.0.1.94
    6  cd
    7  cat /etc/hosts
    8  ping worker-node-1
    9  ping worker-node-2
   10  setenforce 0
   11  sed -i --follow-symlinks 's/SELINUX=enforcing/SELINUX=disabled/g' /etc/sysconfig/selinux
   12  firewall-cmd --permanent --add-port=6443/tcp
   13  yum install firewall
   14  yum install firewalld
   15  firewall-cmd --permanent --add-port=6443/tcp
   16  systect start firewalld
   17  systect start firewall
   18  systemctl start firewall
   19  systemctl start firewalld
   20  systemctl status firewalld
   21  firewall-cmd --permanent --add-port=6443/tcp
   22  systemctl enable firewalld
   23  firewall-cmd --permanent --add-port=2379-2380/tcp
   24  firewall-cmd --permanent --add-port=10250/tcp
   25  firewall-cmd --permanent --add-port=10251/tcp
   26  firewall-cmd --permanent --add-port=10252/tcp
   27  firewall-cmd --permanent --add-port=10255/tcp
   28  firewall-cmd –reload
   29  firewall-cmd reload
   30  firewall-cmd man
   31  firewall-cmd man page
   32  modprobe br_netfilter
   33  netstat -a
   34  netstat -aanlp
   35  netstat -anl
   36  echo '1' > /proc/sys/net/bridge/bridge-nf-call-iptables
   37  cat <<EOF > /etc/yum.repos.d/kubernetes.repo
   38  [kubernetes]
   39  name=Kubernetes
   40  baseurl=https://packages.cloud.google.com/yum/repos/kubernetes-el7-x86_64
   41  enabled=1
   42  gpgcheck=1
   43  repo_gpgcheck=1
   44  gpgkey=https://packages.cloud.google.com/yum/doc/yum-key.gpg https://packages.cloud.google.com/yum/doc/rpm-package-key.gpg
   45  EOF
   46  yum install kubeadm docker -y 
   47  systemctl enable kubelet
   48  systemctl start kubelet
   49  systemctl enable docker
   50  systemctl start docker
   51  swapoff -a
   52  kubeadm init
   53  netstat -a |grep 10250
   54  firewall-cmd -reload
   55  firewall-cmd --reload
   56  netstat -a |grep 10250
   57  netstat 
   58  netstat -tunlp |grep 6443
   59  kubeadm init
   60  kubeadm init
   61  vi /etc/udev/rules.d/70-persistent-net.rules
   62  kubeadm init
   63  mkdir -p $HOME/.kube
   64    sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
   65    sudo chown $(id -u):$(id -g) $HOME/.kube/config
   66  kubeadm join 10.0.1.82:6443 --token osglmr.humxzmuopujajdx4     --discovery-token-ca-cert-hash sha256:6e997a9e308b12e0f5cf3a59b030fbc5ccb88372917b4fc1df066829df85fe52 
   67  kubeadm join 10.0.1.82:6443 --token osglmr.humxzmuopujajdx4 --discovery-token-ca-cert-hash sha256:6e997a9e308b12e0f5cf3a59b030fbc5ccb88372917b4fc1df066829df85fe52 
   68  kubeadm join 10.0.1.82:6443 --token osglmr.humxzmuopujajdx4 --discovery-token-ca-cert-hash sha256:6e997a9e308b12e0f5cf3a59b030fbc5ccb88372917b4fc1df066829df85fe52 
   69  kubectl get nodes
   70  export kubever=$(kubectl version | base64 | tr -d '\n')
   71  kubectl apply -f https://raw.githubusercontent.com/coreos/flannel/master/Documentation/kube-flannel.yml
   72  kubectl get node
   73  kubectl get node
   74  kubectl get nodes
   75  kubectl get nodes
   76  kubectl get nodes
   77  kubectl get nodes
   78  kubectl get node
   79  history 

One Worker Node 1: 10.0.1.16

 1  vim /etc/hosts
    2  yum install firewalld
    3  systemctl start firewalld.service 
    4  systemctl enable firewalld.service 
    5  setenforce 0
    6  sed -i --follow-symlinks 's/SELINUX=enforcing/SELINUX=disabled/g' /etc/sysconfig/selinux
    7  firewall-cmd --permanent --add-port=6783/tcp
    8  firewall-cmd --permanent --add-port=10250/tcp
    9  firewall-cmd --permanent --add-port=10255/tcp
   10  firewall-cmd --permanent --add-port=30000-32767/tcp
   11  firewall-cmd  --reload
   12  echo '1' > /proc/sys/net/bridge/bridge-nf-call-iptables
   13  echo '1' > /proc/sys/net/bridge/bridge-nf-call-iptables
   14  systemctl status firewalld.service 
   15  systemctl restart firewalld.service 
   16  echo '1' > /proc/sys/net/bridge/bridge-nf-call-iptables
   17  cat <<EOF > /etc/yum.repos.d/kubernetes.repo
[kubernetes]
name=Kubernetes
baseurl=https://packages.cloud.google.com/yum/repos/kubernetes-el7-x86_64
enabled=1
gpgcheck=1
repo_gpgcheck=1
gpgkey=https://packages.cloud.google.com/yum/doc/yum-key.gpg https://packages.cloud.google.com/yum/doc/rpm-package-key.gpg
EOF

   18  yum install kubeadm docker -y 
   19  systemctl enable docker
   20  systemctl start docker
   21  systemctl enable kubelet
   22  systemctl start kubelet
   23  kubeadm join 10.0.1.82:6443 --token osglmr.humxzmuopujajdx4 --discovery-token-ca-cert-hash sha256:6e997a9e308b12e0f5cf3a59b030fbc5ccb88372917b4fc1df066829df85fe52 
   24  history 

On Worker Node -2 : 10.0.1.94
   22  vim /etc/hosts
   23  yum install firewalld
   24  systemctl start firewalld.service d
   25  systemctl start firewalld.service 
   26  systemctl status firewalld.service 
   27  systemctl enable firewalld.service 
   28  setenforce 0
   29  sed -i --follow-symlinks 's/SELINUX=enforcing/SELINUX=disabled/g' /etc/sysconfig/selinux
   30  firewall-cmd --permanent --add-port=6783/tcp
   31  firewall-cmd --permanent --add-port=10250/tcp
   32  firewall-cmd --permanent --add-port=10255/tcp
   33  firewall-cmd --permanent --add-port=30000-32767/tcp
   34  firewall-cmd  --reload
   35  echo '1' > /proc/sys/net/bridge/bridge-nf-call-iptables
   36  cat <<EOF > /etc/yum.repos.d/kubernetes.repo
[kubernetes]
name=Kubernetes
baseurl=https://packages.cloud.google.com/yum/repos/kubernetes-el7-x86_64
enabled=1
gpgcheck=1
repo_gpgcheck=1
gpgkey=https://packages.cloud.google.com/yum/doc/yum-key.gpg https://packages.cloud.google.com/yum/doc/rpm-package-key.gpg
EOF

   37  yum install kubeadm docker -y 
   38  systemctl enable docker
   39  systemctl start docker
   40  systemctl enable kubelet
   41  systemctl start kubelet
   42  kubeadm join 10.0.1.82:6443 --token osglmr.humxzmuopujajdx4 --discovery-token-ca-cert-hash sha256:6e997a9e308b12e0f5cf3a59b030fbc5ccb88372917b4fc1df066829df85fe52 
   43  kubeadm join 10.0.1.82:6443 --token osglmr.humxzmuopujajdx4 --discovery-token-ca-cert-hash sha256:6e997a9e308b12e0f5cf3a59b030fbc5ccb88372917b4fc1df066829df85fe52 
   44  history 
   
   
   Output of Cluster:
   
   [root@ip-10-0-1-82 ec2-user]# kubectl get nodes -o wide
NAME                                      STATUS   ROLES    AGE     VERSION   INTERNAL-IP   EXTERNAL-IP   OS-IMAGE         KERNEL-VERSION                  CONTAINER-RUNTIME
ip-10-0-1-16.us-east-2.compute.internal   Ready    <none>   2d14h   v1.19.2   10.0.1.16     <none>        Amazon Linux 2   4.14.193-149.317.amzn2.x86_64   docker://19.3.6
ip-10-0-1-82.us-east-2.compute.internal   Ready    master   2d14h   v1.19.2   10.0.1.82     <none>        Amazon Linux 2   4.14.193-149.317.amzn2.x86_64   docker://19.3.6
ip-10-0-1-94.us-east-2.compute.internal   Ready    <none>   2d14h   v1.19.2   10.0.1.94     <none>        Amazon Linux 2   4.14.198-152.320.amzn2.x86_64   docker://19.3.6
