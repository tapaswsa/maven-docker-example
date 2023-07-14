def BRANCH = 'master'

pipeline {
    agent any
    stages {
        stage ('SCM') {
            steps {
               script {    
                   git branch: "${BRANCH}", credentialsId: 'tapaswini-github-creds', url: 'https://github.com/tapaswsa/maven-docker-example.git'
               } 
            }
        }
        stage ('Build') {
            when {
                expression {
                    "${BRANCH}" == 'master';
                }   
            }
            steps {
              echo "Build"
            }
        }
        
        stage ('Test') {
            when {
                expression {
                    "${BRANCH}" == 'developer';
                }   
            }
            steps {
              echo "Test"
            }
        }
        stage ('Deploy') {
            when {
                expression {
                    "${BRANCH}" == 'master';
                }   
            }
            steps {
                echo "Deploy"
            }
        }
    }
}
