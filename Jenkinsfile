pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    } 
    environment {
        GREETING = 'Hello Jenkins'
    }

    // BUILD
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                // echo 'Deploy'
                sh """
                    echo "Here I Wrtote Shell Script"
                    echo "$GREETING"

                """
            }
        }
    }

    // POST BUILD
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
         failure { 
            echo 'This runs when pipeline is failed, used set alert'
        }
         success { 
            echo 'This runs when pipeline is SUCCESS'
        }
    }
}