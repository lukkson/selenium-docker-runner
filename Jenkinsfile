pipline{
	agent any
	stages{
		stage("Run Test"){
			step{
				sh "docker-compose up"	
			}
		}
		stage("Bring Grrid down"){
			step{
				sh "docker-compose dow"
			}
		}
	}
}