pipeline {
        agent any

    stages {
        stage('Cloning Git Repo') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/dev']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/hamza333-tech/jenkins.git']]])
            }    
        }
        stage('ElasticBeanstalk trigger') {
            steps {
                 sh "/usr/local/aws-cli ec2 describe-instances"
            }    
        }
    }          
}


