pipeline {
    agent any
    tools {
        maven 'MAVEN_HOME' 
    }
    stages {
        stage('Hello My Java App'){
            steps{
                echo 'Java app up'
            }
        }
        stage('Clone the repo'){
            steps{
                git branch: 'master', url:'https://github.com/shohail-DeV/jenkins-example.git'
            }
        }
        stage ('Compile Stage') {
            steps {
                    bat 'mvn clean compile'
            }
        }
        stage ('Testing Stage') {
            steps {
                    bat 'mvn test'
            }
        }
        stage('Code restoration'){
            steps{
                bat 'mvn clean'
            }
        }
        stage ('Artifact') {
            steps {
                    bat 'mvn clean install'
            }
        }
    }
}