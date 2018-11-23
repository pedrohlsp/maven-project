pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                echo 'ta aqui'
                sh 'ls -la'
                sh 'cat Jenkinsfile'
                sh 'mvn clean package'
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