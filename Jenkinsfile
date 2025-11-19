pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/FouedBenRhayem/test_jinkins.git'
            }
        }

        stage('Clean') {
            steps {
                sh 'rm -rf target'
            }
        }

        stage('Compile') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}

