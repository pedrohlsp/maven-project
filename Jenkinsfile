pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                bat 'mvn Clean package_jenkinsfile'
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