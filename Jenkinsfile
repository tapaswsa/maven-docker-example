def BRANCH = 'master'

pipeline {
    agent any
    stages {

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
                    "${BRANCH}" == 'master';
                }   
            }
            steps {
              echo "Test"
            }
        }
        stage ('Deploy') {
            when {
                expression {
                    "${BRANCH}" == 'production';
                }   
            }
            steps {
                echo "Deploy"
            }
        }

    }
}
