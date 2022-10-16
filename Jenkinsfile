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
                    sh "eb deploy Nodesampleapplication-env"
            } 
            
        }
    }          
}


