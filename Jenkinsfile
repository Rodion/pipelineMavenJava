pipeline {
  agent any
    tools {
        maven 'Maven_3.5.2' 
    }
  stages {
    stage('Build') {
      agent any
      steps {
        git(url: 'https://github.com/Rodion/ComeAndEat.git', branch: 'master')
        withMaven() {
          sh 'mvn clean verify'
        }

      }
    }

  }
}