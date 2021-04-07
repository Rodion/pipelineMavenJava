pipeline {
  agent any
  environment {
        registry = 'mafiozi/jenkins-test'
        registryCredential = 'dockerhub'
        dockerImage = ''
  }
  stages {
    stage('Build') {
      agent any
      steps {
        git(url: 'https://github.com/Rodion/ComeAndEat.git', branch: 'master')
        withMaven() {
          sh 'mvn clean install -DskipTests -Dmaven.test.skip=true'
        }

      }
    }

    stage('Test') {
      steps {
        git 'https://github.com/Rodion/ComeAndEat.git'
        withMaven() {
          sh 'mvn test'
        }

      }
    }

    stage('Copy Jar') {
    }
 
    /*
    stage('Docker') {
      agent {
          docker {
              image 'docker'
          }
      }
      steps {
          sh 'docker --version'
      }
    }
    stage('Building our image') {
        steps{
            script {
                dockerImage = docker.build registry + ":$BUILD_NUMBER"
            }
              echo "Build number #${env.BUILD_NUMBER}"
        }
    }
    stage('Deploy our image') {
        steps{
            script {
                docker.withRegistry( '', registryCredential ) {
                    dockerImage.push()
                }
            }
        }
    }
    stage('Cleaning up') {
        steps{
            sh "docker rmi $registry:$BUILD_NUMBER"
        }
    }
    */
  }
}