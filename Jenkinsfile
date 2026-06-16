pipeline{
	agent any
	
	tools{
		maven 'Maven'
	}
	
	stages{
		stage('Checkout'){
			steps{
				git branch:'master', url:'https://github.com/harmain27-04/1stone.git'
			}
		}
		stage('Build'){
			steps{
				sh 'mvn clean package'
			}
		}
		stage('Test'){
			steps{
				sh 'mvn test'
			}
		}
		stage('Run Application'){
			steps{
				sh 'java -jar target/1stone-1.0-SNAPSHOT.jar'
			}
		}
	}
	post{
		success{
			echo 'build successfully'
		}
		failure{
			echo 'builf failure'
		}
	}
}
			
		

