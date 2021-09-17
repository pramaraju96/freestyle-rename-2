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
                    snDevOpsChange(changeRequestDetails:"""{
                          "setCloseCode":false,
                          "attributes":{
                             "requested_by":{
                                "name":"System Administrator"
                             },
                             "assigned_to":"a0e11bb23ba32300b200655593efc491",
                             "category":"Service",
                             "sys_created_on":"2021-02-09 18:58:41",
                             "start_date": "2021-02-09 18:58:41",
                             "end_date": "2022-02-09 18:58:41",
                             "priority":"1",
                          }
                    }""")
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
