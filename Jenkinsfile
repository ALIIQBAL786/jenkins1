pipeline {
    agent any
    environment {
        name = "ALI IQBAL"
    }
    parameters {
        string(name: 'Person', defaultValue: "Babar", description: "Who are you?")
        booleanParam(name: 'isMale', defaultValue: true, description: "Are you a male?")
        choice(name: 'City', choices: ['Jaipur', 'Mumbai', 'Pune'], description: "Select a city")
    }
    stages {
        stage('Run A command') {
            steps {
                sh '''
                ls 
                date
                pwd
                echo "$name"
                '''
            }
        }
        stage('Environment variable') {
            environment {
                username = "USAMA IQBAL"
            }
            steps {
                sh "echo \"$BUILD_ID\""
                sh "echo \"$username\""
            }
        }
        stage('Parameters') {
            steps {
                sh "echo \"$isMale\""
                sh "echo \"$City\""
            }
        }
        stage('Deploy on test') {
            steps {
                echo 'Deploy on Test'
            }
        }
        stage('Continue?') {
            steps {
                input message: "Should we continue?", ok: "We should do"
                echo 'Continuing after input'
            }
        }
        stage('Deploy on prod') {
            steps {
                git clone https:////
                echo 'Deploy on Production'
            }
        }
    }
    post{
        always{
            echo "I will always say Hello"
        }
        failure{
            echo "Failure"
        }
        success{
            echo "Success"
        }
    }
}
