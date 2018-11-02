pipeline {
    agent {
        docker {
            image '8.12.0-alpine' 
            args '-p 4200: 4200' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
		sh 'npm i -g @angular/cli'
		sh 'ng build'
            }
        }
    }
}