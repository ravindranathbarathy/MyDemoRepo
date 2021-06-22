pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh "echo Running under $STAGE_NAME"
                Response = httpRequest consoleLogResponseBody: true, responseHandle: 'NONE', url: 'https://api.github.com/repos/jenkinsci/jenkins/pulls', wrapAsMultipart: false
                echo "${Response}"
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