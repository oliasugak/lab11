pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '-v $HOME/.m2:/root/.m2'
    }
  }
  stages {
    stage('Build') {
      steps {
       sh 'cd /var/jenkins_home'
       sh 'mvn clean install'
       
      }
    }
  }
}

