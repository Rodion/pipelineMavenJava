pipeline {
  agent none
  stages {
    stage('Build') {
      agent any
      steps {
        git(url: 'https://github.com/Rodion/ComeAndEat.git', branch: 'main', changelog: true, poll: true)
        sh '''git url: \'https://github.com/cyrille-leclerc/multi-module-maven-project\'
withMaven {
      sh "mvn clean verify"
}'''
      }
    }

  }
}