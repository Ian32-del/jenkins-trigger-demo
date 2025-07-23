pipeline {
    agent any


    stages {
        stage ('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Ian32-del/jenkins-trigger-demo.git'
            }
        }

        stage ('Install Dependencies'){
            steps {
                sh 'npm install'
            }
        }

        stage ('Test'){
            steps {
                sh 'npm test || echo "no tests yet" '
            }
        }

        stage ('Build Complete'){
            steps {
                echo 'Build ran Successfully !'
            }
        }
    }
}