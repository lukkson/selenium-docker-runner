pipeline{
	agent any
	stages{
		stage("Pull Latest Image") {
			steps{
				bat "docker pull lakilo/selenium-docker"
			}
		}
		stage("Start Grid"){
			steps{
				bat "docker-compose up -d hub chrome firefox"	
			}
		}
		stage("Run Test"){
			steps{
				bat "docker-compose up search-module search-flight-module"	
			}
		}
	}
	post {
		always {
            archiveArtifacts artifacts: 'output/**'
            bat "docker-compose down"
		}
	}
}