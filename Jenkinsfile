pipeline {
    agent {
        docker {
            image 'node:20'
            args '-u root'
        }
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out repository'
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }
    }
}

