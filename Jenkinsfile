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
        maven {
          sh "mvn clean verify"
        }// withMaven will discover the generated Maven artifacts, JUnit Surefire & FailSafe reports and FindBugs reports
      }
    }

  }
}