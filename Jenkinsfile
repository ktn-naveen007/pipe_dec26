pipeline {
    agent { 
        node { label 'Node_Ub' } 
        agent{image 'ubuntu:15.04'}
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