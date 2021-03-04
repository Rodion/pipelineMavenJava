pipeline {
  agent none
  stages {
    stage('Build') {
      agent any
      steps {
        git(url: 'https://github.com/Rodion/ComeAndEat.git', branch: 'main', changelog: true, poll: true)
        sh '''withMaven {
      sh "mvn clean verify"
}'''
        }
      }

    }
  }