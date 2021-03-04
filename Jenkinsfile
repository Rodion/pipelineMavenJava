pipeline {
  agent none
  stages {
    stage('Build') {
      agent {
        node {
          label 'Git fetch project'
        }

      }
      steps {
        git(url: 'https://github.com/Rodion/ComeAndEat.git', branch: 'main', changelog: true, poll: true)
        sh 'mvn clean install'
      }
    }

  }
}