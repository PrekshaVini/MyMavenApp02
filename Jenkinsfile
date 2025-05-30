pipeline{
	agent any
	
	tools{
	maven 'Maven'
	}
	
	stages{
		stage('Checkout'){
			steps{
				sh 'https://github.com/PrekshaVini/MyMavenApp02'
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
				sh 'java -jar target/MyMavenApp02-1.0-SNAPSHOT.jar'
			}
		}
		}
		
		post{
			success{
				echo 'Build and deployment successful!'
				}
			failure{
				echo 'Build failed'
				}
		}
}
	
