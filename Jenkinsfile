pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh "echo Running under $STAGE_NAME"
                def response = httpRequest url: 'https://api.github.com/repos/jenkinsci/jenkins/pulls'
                echo "${response}"
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