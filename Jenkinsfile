pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh npm install mocha -g
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh mocha --recursive -R xunit test/ > test-reports.xml
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
