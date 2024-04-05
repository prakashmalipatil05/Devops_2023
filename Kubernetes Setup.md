# Commands to install kunernetes in Master & Worker Nodes
- sudo su
- yum install docker -y
- systemctl enable docker
- systemctl start docker
  
# Link for install kubeadm kubernetes
- https://v1-27.docs.kubernetes.io/docs/setup/production-environment/tools/kubeadm/install-kubeadm/

# Install kubelet, kubeadm and kubectl, and enable kubelet to ensure it's automatically started on startup:

- sudo yum install -y kubelet kubeadm kubectl --disableexcludes=kubernetes
- sudo systemctl enable --now kubelet
- 
# In Master Node
- kubeadm init

# initailizing and generating token and this type 3 commands paste in master only
# example 
- mkdir -p $HOME/.kube
  sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
  sudo chown $(id -u):$(id -g) $HOME/.kube/config
  export KUBECONFIG=/etc/kubernetes/admin.conf

# Worker 
  # in master generated token paste in Worker Node
  # Example
  - kubeadm join 172.31.36.81:6443 --token drw2rf.lw3glgl83b060anz \
        --discovery-token-ca-cert-hash sha256:ea8c30733f760966283d700ee19e1a8036e1d47b0745054aa1529b66fe4007ed

    # Afterthat install calico in Master Node
    - curl https://raw.githubusercontent.com/projectcalico/calico/v3.27.3/manifests/calico.yaml -O
    - kubectl apply -f calico.yaml
# its shows node status ready or not ready
- kubectl get nodes

# Pods creating Command
- kubectl run pod1 --image=nginx
- kubectl get pods

# for showing ip address of pods and worker nodes
- kubectl get pods -o wide
   
    
