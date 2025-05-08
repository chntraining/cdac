pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                echo 'Cloning the repository'
                git branch: 'main', url: 'https://github.com/chntraining/cdac.git', credentialsId: 'mygithubcred'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the Application'
                bat 'hello.bat'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Tests'
                bat 'echo All TEST CASES PASSSSSSSED'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the Application'
                bat 'echo Deployment SUCCESSFUL'
            }
        }
    }

    post { 
        always { 
            echo 'Pipeline execution Completed Successfully :) !'
        }
    }
}
