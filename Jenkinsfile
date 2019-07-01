pipeline {
    agent none
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
