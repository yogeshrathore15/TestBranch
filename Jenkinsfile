pipeline {
    agent { docker 'ubuntu:latest'}
    stages {
        stage('SourceCode') {
            steps {
                checkout scm
            }
        }
        stage('Deliver to staging') {
            when {
                branch 'dev' 
            }
            steps {
                cat Develope
            }
        }
        stage('Deploy to production') {
            when {
                branch 'master'  
            }
            steps {
                cat Production
            }
        }
    }
}
