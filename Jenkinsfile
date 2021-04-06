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

  }
}