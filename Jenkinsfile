pipeline {
    agent any
    tools{
        maven 'maven'
    }
    
    stages{
        stage('Build Maven'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Phani808/-kubernetes_java_deployment.git']]])
                sh 'mvn clean install'
            }
        }
    } 
} 
