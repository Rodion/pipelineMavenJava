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

        sh 'cp ./target/comeandeat-0.0.1-SNAPSHOT.jar /data/comeandeat.jar'
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
    test = 'test'
  }
}