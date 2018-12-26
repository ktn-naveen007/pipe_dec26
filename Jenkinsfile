pipeline {

    agent   { label 'Node_Ub' }                                                                            
                 
        
    stages {

            stage('Back-end') {
            agent {
                docker{image 'ubuntu:15.04'}
            }
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