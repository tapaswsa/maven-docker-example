pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
               echo "Build"
            }
        }
        
        stage ('Test') {
            steps {
               echo "Test"
            }
        }
        
        stage ('Sonar Scan for Feature') {
            when {
                branch "feature/*"
            }
	    steps {
                echo "Sonar Scan for Feature" 
            }
        }

        stage ('Sonar Scan for PR') {
            when {
                branch "PR*"
            }
	    steps {
                echo "Sonar Scan for PR" 
            }
        }

        stage ('Deploy') {
            steps {
                echo "Deploy" 
            }
        }
    }
    post { 
        cleanup { 
            echo "Clean up in post workspace"
            cleanWs()
        }
    }
}   
