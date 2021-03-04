pipeline {
  agent none
  stages {
      stage ('Build') {
        git(url: 'https://github.com/Rodion/ComeAndEat.git', branch: 'main', changelog: true, poll: true)
        withMaven {
          sh "mvn clean verify"
        } // withMaven will discover the generated Maven artifacts, JUnit Surefire & FailSafe reports and FindBugs reports
      }
    }
  }
}
