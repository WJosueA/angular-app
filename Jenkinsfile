pipeline {
    agent {
        label "windows-worker"
    }

    stages {
        stage('Angular Verification') {
            steps {
                bat "ng version"
            }
        }
        
        stage('Initialize Terraform'){
           steps {
                 bat "terraform init"
             }
        }

         stage('Create Infrastructure AWS Terraform'){
             steps {
                 bat "terraform apply --auto-approve"
             }
        }
    }
}
