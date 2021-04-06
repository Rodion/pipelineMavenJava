pipeline {
  agent any
  stages {
    stage('Build') {
      agent any
      steps {
        git(url: 'https://github.com/Rodion/ComeAndEat.git', branch: 'master')
        withMaven() {
          sh 'mvn clean install -DskipTests -Dmaven.test.skip=true'
        }

      }
    }

  }
<<<<<<< HEAD
}
=======
  tools {
    maven 'Maven_3.6.3'
  }
}
>>>>>>> 180620be333f048667c6de47616f79e8733f8caf
