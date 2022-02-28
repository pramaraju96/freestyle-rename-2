pipeline {
    agent any
    tools {
    	maven 'Maven'
    }
    stages {        
        stage('Build') {           
            steps {
                snDevOpsChange()
                echo 'Building...'
                echo "Change approved and implemented"
            }
        }
        stage('Test') {
            agent any 
            steps {
                echo 'Testing...'
            }
        }
      stage('Deploy') {
              agent any
              steps {
                  snDevOpsChange()
                  echo 'Deploying...'
                  echo "Change approved"
              }
          }
    }
}
