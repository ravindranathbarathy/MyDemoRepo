pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh "echo Running under $STAGE_NAME"
                def res=httpRequest url: 'https://api.github.com/repos/jenkinsci/jenkins/pulls'
                echo "${res}"
            }
        }
        stage('Test') {
            steps {
                sh "echo Running under $STAGE_NAME"
            }
        }
        stage('Deliver') {
            steps {
                sh "echo Running under $STAGE_NAME"
            }
        }
    }      
}