pipeline {
    agent {
        kubernetes {
          label " jenkins-agent-main"
        }
        }
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Sleep') {
            steps {
                sleep 10
            }
        }
        stage('Run') {
            steps {
                sh 'uname -a'
            }
        }
    }
    
}
