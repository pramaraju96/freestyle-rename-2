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
                options {
                timeout(time: 24, unit: "HOURS")
                }
                echo "Building..."
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
