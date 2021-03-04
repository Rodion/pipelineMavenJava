pipeline {
  agent none
  stages {
    stage('Git') {
      agent any
      steps {
        git(url: 'https://github.com/Rodion/ComeAndEat.git', branch: 'main')
      }
    }

  }
}