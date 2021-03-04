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
          script {
            node {
              stage ('Build') {
                git url: 'https://github.com/cyrille-leclerc/multi-module-maven-project'
                withMaven {
                  sh "mvn clean verify"
                } // withMaven will discover the generated Maven artifacts, JUnit Surefire & FailSafe reports and FindBugs reports
              }
            }
          }

        }
      }

    }
  }