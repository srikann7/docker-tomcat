pipeline {
    environment {
    PATH = "C:\Program Files\Git\usr\bin;C:\Program Files\Git\bin;"
    agent any
    stages{
        stage('Build'){
            steps {
                    sh 'mvn clean package'
                  }
             post {
                success{
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
             }
            }
        }
    }
 }  
