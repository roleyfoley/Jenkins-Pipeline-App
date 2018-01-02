pipeline {
    agent {    
    }
    
    stages {
        stage('Test') {
            node { 
                docker.withServer{'tcp://192.168.99.100:2376', 'LocalDockerHost') {
                    docker.image('node:7-alpine')
                }
            }
            steps {
                sh 'node --version'
                sh 'echo Hello Folks'
            }
        }
    }
}