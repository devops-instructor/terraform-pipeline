pipeline {
    agent {
        docker {
            image 'hashicorp/terraform:1.15.2'
        }
    }
    stages {      
        stage('init') {
            steps {
                sh 'env | sort'
                sh 'terraform --version'
            }
        }
    }
}