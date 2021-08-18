pipeline {
    agent { label 'maven' }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'java -version'
                sh 'mvn -v'
							  sh 'mvn clean package -DskipTests=true'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    post {
				always {
						cleanWs()
				}
		}
}
