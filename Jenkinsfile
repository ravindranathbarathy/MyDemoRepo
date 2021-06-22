pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh "echo Running under $STAGE_NAME"
                // httpRequest consoleLogResponseBody: true, responseHandle: 'NONE', url: 'https://api.github.com/repos/jenkinsci/jenkins/pulls', wrapAsMultipart: false
                def get = new URL("https://api.github.com/repos/jenkinsci/jenkins/pulls").openConnection();
                def getRC = get.getResponseCode();
                println(getRC);
                if (getRC.equals(200)) {
                    println(get.getInputStream().getText());
}
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