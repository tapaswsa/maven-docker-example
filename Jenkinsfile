def BRANCH = 'staging'

pipeline {
    agent any
    stages {

        stage ('Build') {
            when {
                expression {
                    "${BRANCH}" == 'staging';
                }   
            }
            steps {
              echo "Build"
            }
        }
        
        stage ('Test') {
            when {
                expression {
                    "${BRANCH}" == 'production';
                }   
            }
            steps {
              echo "Test"
            }
        }
        stage ('Deploy') {
            when {
                expression {
                    "${BRANCH}" == 'staging';
                }   
            }
            steps {
                echo "Deploy"
            }
        }

    }
}
