pipeline {
        agent any
	
    tools {
    nodejs 'nodejs'
  }


    stages {
        stage('Cloning Git Repo') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/dev']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/hamza333-tech/jenkins.git']]])
            }
        }
    }          
}


