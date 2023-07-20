pipeline {
    agent any

    environment {
        ENV_URL = "pipeline.google.com"
    }

    stages {

        stage('Stage One') {

            steps {

                sh '''
                    echo DevOps
                    echo AWS Training
                    echo Mukesh Batch54
                    echo Name of the URL is ${ENV_URL}
                '''
            }
        }

        stage('Stage Two') {

            steps {

                echo "This is stage two"
            }
        }

        stage('Stage Three') {

            steps {

                echo "This is stage three"
            }
        }
    }
}