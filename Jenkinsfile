pipeline {
    agent { node { label 'master' } }
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