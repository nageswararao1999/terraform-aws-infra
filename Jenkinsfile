pipeline {
    agent any

    environment {
        GIT_CREDENTIALS = 'git-hub-pat' // Replace with your Jenkins credentials ID
    }

    stages {
        stage('Clone Repository') {
            steps {
                git credentialsId: "${GIT_CREDENTIALS}", url: 'https://github.com/nageswararao1999/terraform-aws-infra.git', branch : 'main'
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
