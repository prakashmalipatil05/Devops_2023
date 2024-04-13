# REPLICA CONROLL AND REPLICA SET
# write file in Yaml file
- examle vi myrc.yml
# apply after writing
- kubectl apply -f myrc.yml
# shows replicas controller 
- kubectl get rc
# shows Replicas Set
- kubectl get rs
# for delete pods
- kubectl delete pod pod full name
# Labels check
- kubectl get pods --show-labels
# scale up and scale down replicas control/pods
- kubectl scale --replicas=8 rc=l myname=prakash
# scale up and scale down replicas control/pods
- kubectl scale --replicas=1 rs/replicaset

# DEPLOYMENT
# write deployment file and apply and shows 
- vi mydeploy.yml
- kubectl apply -f mydeploy.yml
- kubectl get deploy
- kubectl get rs
- kubectl scale --replicas=4 deploy mydeployment
- kubectl logs -f pods full name

# Edit or some changes in file os/image
- vim mydeploy.yml
- kubectl -f mydeploy.yml
- kubectl get pods
- kubectl logs -f pods full name

# OS details
- kubectl exec pod name --cat /etc/os-release

# for rollback its unlocks
- kubectl rollout status deployment mydeployments
# history rollouts
- kubectl rollout history deployment mydeployments
# its rollback
- kubectl rollout undo deploy/mydeployments



