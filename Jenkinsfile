pipeline {
    agent any 

    environment {
        PYTHON_FILE = 'helloworld.py'
        JAVASCRIPT_FILE = 'helloworld.js'
    }

    stages{
        stage('Check') {
            date 
            echo 'Committed from ${GIT_LOCAL_BRANCH} branch'
            echo 'Build ID : ${BUILD_ID}'
            echo 'Build URL : ${BUILD_URL}' 
        }
        stage('Run Python Script') {
            step {
                sh 'python3 ${PYTHON_FILE}'
            }
        }
        stage('Run Python Script') {
            step {
                sh 'node ${JAVASCRIPT_FILE}'
            }
        }
        stage('Slack') {
            step {
                slackSend message: 'Done! Testing Python and JavaScript script : )'
            }
        }
    }
}