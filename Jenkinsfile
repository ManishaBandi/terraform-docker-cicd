
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
                bat 'terraform version'
                bat 'terraform init -backend=false'
                bat 'terraform validate'
            }
        }
    }
}
