pipeline {
  agent none
  stages {
    stage('Git') {
      steps {
        git(url: 'https://github.com/Rodion/ComeAndEat.git', branch: 'main', changelog: true, poll: true)
      }
    }

  }
}