pipeline {
    agent any
    tools {
    	maven 'Maven'
    }
    stages {
        
        stage('Build') {
            options {
                timeout(time: 1, unit: 'HOURS') 
            }
            steps {
                echo 'Building..'
                script{
                    snDevOpsChange()
                }
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
