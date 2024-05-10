pipeline {
    agent any

    environment {
        TOMCAT_HOME = '/var/lib/tomcat8'
    }

    tools {
        maven 'Maven'
    }
    
    stages {
        
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'mvn clean package'
                sh 'ls -l target'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying..'
                sh 'pwd'
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'Success!'
        }
        failure {
        }
        unstable {
        }
        changed {
        }
    }
}
