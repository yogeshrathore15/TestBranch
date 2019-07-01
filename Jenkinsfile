pipeline {
    agent {
        docker {
            image 'ubuntu:latest'
            args '-p 80:80' 
        }
    }
    stages {
        stage('SourceCode') {
            steps {
                checkout scm
            }
        }
        stage('Deliver for staging') {
            when {
                branch 'dev' 
            }
            steps {
                cat Develope
            }
        }
        stage('Deploy for production') {
            when {
                branch 'master'  
            }
            steps {
                cat Production
            }
        }
    }
}
