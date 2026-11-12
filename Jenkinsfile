pipeline {
    agent any

    environment {
        PATH = "C:\\Users\\HP\\AppData\\Local\\Programs\\DockerDesktop\\resources\\bin;${env.PATH}"
    }

    stages {
        stage('build image') {
            steps {
                echo 'Building the Docker image...'
                bat 'docker build -t arvind-jenkins-demo-image .'
            }
        }

        stage('Run Docker Container') {
            steps {
                echo 'Starting the container...'
                bat 'docker rm -f arvind-jenkins-demo-container || exit 0'
                bat 'docker run -d --name arvind-jenkins-demo-container -p 8081:80 arvind-jenkins-demo-image'
            }
        }
    }
}
