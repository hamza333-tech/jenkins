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
                 
                 sh "aws elasticbeanstalk create-application --application-name nodejs-application"
            } 
        }
        stage ('ElasticBeanstalk environment creation') {
            steps {
                 sh "aws elasticbeanstalk create-environment --application-name nodejs-application --environment-name nodejs-application-env --version-label version-1 --solution-stack-name '64bit Amazon Linux 2 v5.6.0 running Node.js 16'"
            }
            
        }
    }          
}


