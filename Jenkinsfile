pipeline {
    agent any
    environment {
        ENV_URL         = "pipeline.google.com"             // Global variable or pipeline variable. Every stage can use when declared here.
        SSHCRED   = credentials('SSH_CRED')
    }

    stages {
        stage('Stage One') {
            steps {
                sh '''
                    echo DevOps
                    echo AWS Training
                    echo Mukesh Batch54
                    echo Name of the URL is ${ENV_URL}

                    env 
                '''
            }
        }

        stage('Stage Two') {
            environment {
            ENV_URL = "stage.google.com"            // Stage variable.
            }
            steps {

                echo "This is stage two"
                echo "Name of the URL is ${ENV_URL}"
            }
        }

        stage('Stage Three') {
            steps {
                echo "This is stage three"
                echo "Name of the URL is ${ENV_URL}"
                sh "echo -e \\e[32m Hello! \\e[0m"
            }
        }
    }
}