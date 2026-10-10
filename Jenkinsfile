
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Check Terraform') {
            steps {
                sh 'terraform version'
                sh 'terraform init -backend=false'
                sh 'terraform validate'
            }
        }
    }
}
