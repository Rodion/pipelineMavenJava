pipeline {
  agent any
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
      steps {
        sh 'cp ComeAndEat.jar target/ComeAndEat.jar'
      }
    }

  }
  environment {
    registry = 'mafiozi/jenkins-test'
    registryCredential = 'dockerhub'
    dockerImage = ''
  }
}