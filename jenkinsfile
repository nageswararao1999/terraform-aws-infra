pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/yourusername/terraform-jenkins-ci-cd.git'
            }
        }

        stage('Initialize Terraform') {
            steps {
                sh 'terraform init'
            }
        }

        stage('Plan Infrastructure') {
            steps {
                sh 'terraform plan'
            }
        }

        stage('Apply Changes') {
            steps {
                sh 'terraform apply -auto-approve'
            }
        }
    }
}
