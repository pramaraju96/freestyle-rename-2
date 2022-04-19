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
                echo "Change approve"
            }
        }
        stage('Test') {
            agent any 
            steps {
                echo 'In Testing stage...'
            }
        }
      stage('Deploy') {
              agent any
              steps {
                  snDevOpsChange()
                  echo 'Deploying...'
                  echo "Change approved and implemented"
              }
          }
    }
}
