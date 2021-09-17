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
        }
        stage('Test') {
            agent any 
            steps {
                echo 'Testing...'
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
