pipeline{
	agent any
	stages{
		stage("Run Test"){
			steps{
				bat "docker-compose up"	
			}
		}
		stage("Bring Grrid down"){
			steps{
				bat "docker-compose dow"
			}
		}
	}
}