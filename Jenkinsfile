pipeline {
    agent any 

    environment {
        PYTHON_FILE = 'helloworld.py'
        JAVASCRIPT_FILE = 'helloworld.js'
    }

    stages{
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
    }
}