pipeline {
  agent any
  stages {
    stage('Build Image') {
      steps {
      echo 'docker build -t arvind-web.'
    }
    }
      stage('run container'){
        steps{
          echo 'docker rm -f arvind-web || true'
          echo 'docker run -d --name arvind-web -p 8081:80 arvind-web'
        }
      }
    }
  }
    
