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
        
        // stage('Initialize Terraform'){
        //     steps {
        //         bat "terraform init"
        //     }
        // }

        // stage('Create Infrastructure AWS Terraform'){
        //     steps {
        //         bat "terraform apply --auto-approve"
        //     }
        // }

        stage('Deploy to AWS S3'){
            steps {
                bat "aws s3 cp C:\\inetpub\\wwwroot\\romell\\dev s3://my-tf-test-bucket-clase7-ucreativa --recursive"
            }
        }
    }
}