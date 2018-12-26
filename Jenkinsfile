pipeline {
    //agent { node { label 'master' } }
    agent{
        docker {image 'openjdk:8-jdk-alpine'}
        }
    stages {
        stage('compile') { 
            steps {
                 bat """
    					mvn compile -Dmaven.skipTests=true
    				"""
            }
        }
        
        stage('Deploy') { 
            steps {
                 bat """
        					mvn package
        				"""
    }
        }
    }
}