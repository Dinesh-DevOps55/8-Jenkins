pipeline {
    agent any
    stages {
        stage('test') {
            steps {
               script {
                   echo 'testing the app'
                   echo 'testing the integration'
               }
            }
        }
        stage('build') {
            steps {
               script {
                   echo 'building the app'
                
               }
            }
        }
        stage('deploy') {
            steps {
                script {
                   echo 'deploying the app'
               }
            }
        }
    }
}

