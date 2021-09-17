pipeline {
    agent any
    tools {
    	maven 'Maven'
    }
    stages {
        stage('Build') {
            agent any 
            steps {
                snDevOpsChange()
                echo "Building..."
            }
            options {
                timeout(time: 24, unit: "HOURS")
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
