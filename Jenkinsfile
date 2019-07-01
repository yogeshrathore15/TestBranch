pipeline {
    agent {
        docker {
            image 'ubuntu-18.04'
            args '-p 3000:3000 -p 80:80' 
        }
    }
    stages {
        stage('SourceCode') {
            steps {
                checkout scm
            }
        }
        stage('Deliver for development') {
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
