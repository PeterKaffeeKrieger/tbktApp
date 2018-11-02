pipeline {
    agent any

    stages {
        stage('Build') { 
            steps {
                sh 'npm install'
		sh 'npm i -g @angular/cli'
		sh 'ng build'
		sh 'npm run electron-build'
            }
        }
    }
}