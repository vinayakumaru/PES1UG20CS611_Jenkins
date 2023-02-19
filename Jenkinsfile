pipeline {
	agent any
	stages {
    	stage('Build') {
        	steps {
            	sh 'g++ -o output test.cpp'
        	}
    	}
    	stage('Test') {
        	steps {
                sh './output'
        	}
    	}
    	stage('Deploy') {
        	steps {
            	sh 'cat test.cpp'
            	//error 'Pipeline Failed'
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