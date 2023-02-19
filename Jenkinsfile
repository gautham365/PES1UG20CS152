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
    	failure{
    		echo 'Pipeline Failed'
    	}
    }
}
