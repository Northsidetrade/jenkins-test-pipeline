pipeline {
    agent {
        docker { image 'python:3.11' }
    }
    stages {
        stage('Build') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                sh 'pytest tests/'
            }
        }
        stage('Deploy') {
            steps {
                sh 'bash scripts/deploy.sh'
            }
        }
    }
}
