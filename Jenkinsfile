pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'g++ -o output code.cpp'
            }
        }
        stage('Test') { 
            steps {
                sh 'cat code.cpp'
            }
        }
        stage('Deploy') { 
            steps {
                sh './output'
//                 error 'Pipeline Failed' 
            }
        }
    }
    post{
        success{
            echo 'Pipeline Success'
        }
    	failure{
    		echo 'Pipeline Failed'
    	}
    }
}
