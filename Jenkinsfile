pipeline {
        agent any

    stages {
        stage('Cloning Git Repo') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/dev']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/hamza333-tech/jenkins.git']]])
            }    
        }
        stage('ElasticBeanstalk application creation') {
            steps {
                 
//                  sh "aws elasticbeanstalk create-application --application-name nodejs-application"
//                     sh "eb use Nodesampleapplication-env"
                    sh "eb init --region eu-west-1 --platform 'Node.js 16 running on 64bit Amazon Linux 2' sample-node-application"
                    sh "eb deploy sample-node-application"
            } 
            
        }
    }          
}


