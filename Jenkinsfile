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
        stage('Env') {
            steps {
                sh 'printenv'
            }
        }
        stage('Env2') {
            agent {
                kubernetes {
                    label " jenkins-agent-spot"
                }
            }
            steps {
                sh 'printenv'
            }
        }
    }
}
