pipeline {
  agent none
  stages {
      stage ('Build') {
        git(url: 'https://github.com/Rodion/ComeAndEat.git', branch: 'main', changelog: true, poll: true)
      }
  }
}
