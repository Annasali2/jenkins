pipeline {
        agent any

    stages {

        stage('ElasticBeanstalk application creation') {
            steps {
//                  sh "aws elasticbeanstalk create-application --application-name nodejs-application"
                    sh "eb init --region us-east-1 --platform 'Node.js 16 running on 64bit Amazon Linux 2' node-sample-application-qa"
                    sh "eb deploy Node-sampleapplication-qa-env"
            } 
        }
        stage('Cleaning Workspace') {
            steps {
                cleanWs()            }    
        }
    }          
}
