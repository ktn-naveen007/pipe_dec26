pipeline {

    agent {
            
        docker{
            image 'maven:3-alpine'
            label 'Node_Ub'
        }
    }                                                                          
                 
        
    stages {

        stage('Back-end'){
           
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