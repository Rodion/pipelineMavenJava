pipeline {
  agent none
  stages {
    stage('Git') {
      agent {
        node {
          label 'Git fetch project'
        }

      }
      steps {
        git(url: 'https://github.com/Rodion/ComeAndEat.git', branch: 'main', changelog: true, poll: true)
      }
    }

  }
}