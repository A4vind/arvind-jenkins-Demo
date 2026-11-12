pipeline {
  agent any
  stages {
    stage('Build Image') {
      steps {
      bat 'docker build -t arvind-web.'
    }
    }
      stage('run container'){
        steps{
          bat 'docker rm -f arvind-web || exit 0'
          bat 'docker run -d --name arvind-web -p 8081:80 arvind-web'
        }
      }
    }
  }
    
