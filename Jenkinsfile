pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                npm install mocha -g
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                mocha --recursive -R xunit test/ > test-reports.xml
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
