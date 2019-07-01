pipeline {
    agent any
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
               sh 'cat Develope'
            }
        }
        stage('Deploy to production') {
            when {
                branch 'master'  
            }
            steps {
                sh 'cat Production'
            }
        }
    }
}
