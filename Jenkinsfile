def gv

pipeline {   
    agent any
    tools {
        maven 'Maven-3.9.6'
    }
    stages {
        stage("init") {
            steps {
                script {
                    gv = load "script.groovy"
                }
            }
        }
        stage("deploy") {
            input {
                message "Select the enviroment to deploy"
                ok "Done"
                parameters {
                    choice(name:"ONE", choices: ['dev', 'staging', 'prod'], description:'')
                    choice(name:"TWO", choices: ['dev', 'staging', 'prod'], description:'')
                }
            }
            steps {
                gv.buildApp()
                echo "Deploying to ${ONE}"
                echo "Deploying to ${TWO}"
            }
        }               
    }
} 
