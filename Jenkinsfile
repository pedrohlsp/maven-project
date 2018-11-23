pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                sh 'cat Jenkinsfile'
                echo 'ta aqui'
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