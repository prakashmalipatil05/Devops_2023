# write file in Yaml file
- examle vi myrc.yml
# apply after writing
- kubectl apply -f myrc.yml
# shows replicas
- kubectl get rc
# for delete pods
- kubectl delete pod pod full name
# Labels check
- kubectl get pods --show-labels
# scale up and scale down replicas/pods
- kubectl scale --replicas=8 rc=l myname=prakash

