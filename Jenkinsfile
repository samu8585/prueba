 pipeline {
	agent any
	stages{
		stage ('Primera inicializacion'){
			steps{
				sh 'echo inicializando...'
			}
		}
               stage ('checando docker'){
			steps{
				sh 'sudo docker ps'
                        }
		}
		stage ('Construir imagen'){
			steps{
				sh 'sudo docker build --tag=php54local .'
				sh 'sudo docker images | grep php54local'
			}
		}
		stage ('Cargar Pagina'){
			steps{
				sh 'sudo docker images | grep php54'
                                sh 'sudo docker-compose down'
				sh 'sudo docker-compose up -d'
			}
		}
	}
}
