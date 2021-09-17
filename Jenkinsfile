pipeline {
    agent any
    tools {
    	maven 'Maven'
    }
    stages {        
        stage('Build') {           
            steps {
                echo 'Building..'
                    snDevOpsChange()
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
                  echo 'Deploying..'
              }
          }
    }
}
