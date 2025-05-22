pipeline{
    agent any
    tools {nodejs "my-nodejs"}
    stages{
        stage("Build"){
            steps{
                nodejs("my-nodejs") {
                    bat 'npm install'
                    bat 'npm run build'
                }
            }
        }
        stage("Start"){
            steps{
                nodejs("my-nodejs") {
                    bat 'npm run start'
                }
                echo "App started successfully"
            }
        }
    }
}