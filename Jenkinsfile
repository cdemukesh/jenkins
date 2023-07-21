pipeline {
    agent any
    environment {
        ENV_URL         = "pipeline.google.com"             // Global variable or pipeline variable. Every stage can use when declared here.
        SSHCRED   = credentials('SSH_CRED')
    }
    // parameters {
    //     string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
    //     text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
    //     booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
    //     choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
    //     password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    // }
    //triggers { cron('*/1 * * * *') }

    
    stages {
        stage('Stage One') {
            steps {
                sh '''
                    echo DevOps
                    echo AWS Training
                    echo Mukesh Batch54
                    echo Name of the URL is ${ENV_URL}
                    sleep 10
                    env 
                '''
            }
        }


        stage('Stage Two') {
            environment {
            ENV_URL = "stage.google.com"            // Stage variable.
            }
            // input {
            //     message "Should we continue?"
            //     ok "Yes, we should."
            //     submitter "alice,bob"
            //     parameters {
            //         string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
            //     }
            //  }
            steps {

                echo "This is stage two"
                echo "Name of the URL is ${ENV_URL}"
                echo "Name of the PERSON is ${PERSON}"
                sleep 10
            }
        }

        stage('Stage Three') {
            when { 
                branch 'dev'
                changeset "**/*.js"
             }
            steps {
                sh '''
                echo "This is stage three"
                echo "Name of the URL is ${ENV_URL}"
                echo -e "\\e[31m Hello!! \\e[0m"
                sleep 10
                '''
            }
        }

        stage('Stage Four') {
            steps {
                sh '''
                echo "This is stage four"
                echo "Name of the URL is ${ENV_URL}"
                echo -e "\\e[31m Welcome!! \\e[0m"
                sleep 10
                '''
            }
        }
    }
}