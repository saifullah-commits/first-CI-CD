pipeline{
    agent any 

    environment {
        VERCEL_TOKEN = cridentials('vercel_token')
    }
    stages {
        stage ('Install'){
            steps {
                bat 'npm install'
            }
        }
        stage('Test'){
            step {
                echo 'skipping tests -no test script found'
            }
        }
        stage ('Build'){
            stepd {
                bat 'npx vercel --prod --yes --token=%VERCEL_TOKEN%'
            }
        }
    }
}