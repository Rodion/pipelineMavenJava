1. The source project.  
It's a java/spring boot base project. Located in github: https://github.com/Rodion/ComeAndEat.git 
2. CI proccess is a Jenkins pipeline.  Source file is a Jenkinsfile. 
3. Docker file and docker-compose are in the docker folder
4. Kubernetis configurations are in k8s folder.


Running instruction.

- kubectl kustomize ./k8s
- kubectl apply -k ./k8s
- docker build -t comeandeatimage ./docker
- docker-compose up -d --build

- run  comeandeat --image=rodion31/comeandeat


kubectl delete all --all -n comeandeat


# Get commands with basic output
kubectl get services                          # List all services in the namespace
kubectl get pods --all-namespaces             # List all pods in all namespaces
kubectl get pods -o wide                      # List all pods in the current namespace, with more details
kubectl get deployment my-dep                 # List a particular deployment
kubectl get pods                              # List all pods in the namespace
kubectl get pod my-pod -o yaml                # Get a pod's YAML

# Describe commands with verbose output
kubectl describe nodes my-node
kubectl describe pods my-pod

# List Services Sorted by Name
kubectl get services --sort-by=.metadata.name
