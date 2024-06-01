pipeline {
    agent any 

    environment {
        PYTHON_FILE = 'helloworld.py'
        JAVASCRIPT_FILE = 'helloworld.js'
    }

    stages {
        stage('Check') {
            steps {
                sh 'date'
                echo "Committed from ${GIT_BRANCH} branch"
                echo "Build ID : ${BUILD_ID}"
                echo "Build URL : ${BUILD_URL}"
            }
        }
        stage('Run Python Script') {
            steps {
                sh 'python3 ${PYTHON_FILE}'
            }
        }
        stage('Run JS Script') {
            steps {
                sh 'node ${JAVASCRIPT_FILE}'
            }
        }
        stage('Slack') {
            steps {
                slackSend message: 'Done! Testing Python and JavaScript script'
            }
        }
    }
}
