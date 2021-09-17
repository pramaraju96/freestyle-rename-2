pipeline {
    agent any
    tools {
    	maven 'Maven'
    }
    stages {
        
        timeout(time: 1, unit: 'HOURS') {
        stage('Build') {
            steps {
                echo 'Building...'
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
