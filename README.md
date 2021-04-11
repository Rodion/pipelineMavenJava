1. The source project.  
It's a java/spring boot base project. Located in github: https://github.com/Rodion/ComeAndEat.git 
2. CI proccess is a Jenkins pipeline.  Source file is a Jenkinsfile. 
3. Docker file and docker-compose are in the docker folder
4. Kubernetis configurations are in k8s folder.


Running instruction.

- cd k8s
- kubectl kustomize .
- cd docker 
- docker-compose up -d --build
