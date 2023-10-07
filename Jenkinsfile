pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/YagudinTimur/vector-role.git']]])
            }
        }
        stage('Molecule Test') {
            steps {
                sh '/usr/local/bin/molecule test'
            }
        }
    }
}
