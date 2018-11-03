pipeline {
    agent {
        docker {
            image 'node:8.12.0-alpine' 
            args '-p 4200:4200' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
		sh 'yarn install'
		sh 'yarn add electron-builder --dev'
		sh 'npm i -g @angular/cli'
		sh 'npm run electron-build'
		sh 'ng build'
		sh 'npm install electron-packager -g'
		sh 'npm install electron-packager --save-dev'
		sh 'yarn dist'
            }
        }
    }
}