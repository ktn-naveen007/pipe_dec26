pipeline {

    agent   { label 'Node_Ub' }                                                                            
                 
        
    stages {
stage('Back-end'){
            agent {
                docker{image 'ubuntu:15.04'}
            }
            steps {
                sh 'mvn --version'
            }
   }
        stage('compile') { 
            steps {
                 sh """
    					mvn compile -Dmaven.skipTests=true
    				"""
            }
        }
        
        stage('Deploy') { 
            steps {
                 sh """
        					mvn package
        				"""
    }
        }
    }
}