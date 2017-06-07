pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                 sh 'sudo npm install -g '
                 sh 'sudo npm install mocha -g'
               // sh npm install mocha -g
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'mocha --recursive -R xunit test/ > test-reports.xml'
                //sh mocha --recursive -R xunit test/ > test-reports.xml
            }
        }
        stage('Collect Results') {
            steps {
                echo 'Collect Results....'
                junit 'test-reports.xml'
            }
        }
   }
}
