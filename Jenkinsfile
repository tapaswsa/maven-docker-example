pipeline {
    agent any
    stages {
        // stage ('SCM') {
        //     steps {
        //        script {    
        //            git branch: "${BRANCH}", credentialsId: 'tapaswini-github-creds', url: 'https://github.com/tapaswsa/maven-docker-example.git'
        //        } 
        //     }
        // }
        //
        stage ('Build') {
            when {
                  branch 'master'             
            }
            steps {
              echo "Build"
            }
        }
        
        stage ('Test') {
            when {
                  branch 'masterr'             
            }
            steps {
              echo "Test"
            }
        }
        stage ('Deploy') {
            when {
                  branch 'master'             
            }
            steps {
                echo "Deploy"
            }
        }
    }
}
