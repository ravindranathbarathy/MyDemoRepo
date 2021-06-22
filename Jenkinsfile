pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    sh "echo Running under $STAGE_NAME"
                    def response = httpRequest 'https://api.github.com/repos/jenkinsci/jenkins/pulls'
                    jsonobj = readJSON text: "${response.content}"
                    // echo "${jsonobj.size()}"
                    jsonobj.each {
                        // echo "${it}"
                        def PR1 = "${it}"
                        it.each
                            echo "${it}"
                            if(it.state == "open") {
                            echo "${PR1.title}"
                        }
                    }
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