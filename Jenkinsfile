pipeline {
    agent any

    tools{
        maven 'localMaven'
    }

    stages{
        stage('Build'){
            steps {
                bat 'mvn clean package_jenkinsfile'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }        
    }
}