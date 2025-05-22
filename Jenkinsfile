pipeline{
    agent any
    tools {nodejs "my-nodejs"}
    stages{
        stage("Build"){
            steps{
                nodejs("my-nodejs") {
                    bat 'npm install'
                    bat 'npm build'
                }
            }
        }
        stage("Start"){
            steps{
                nodejs("my-nodejs") {
                    bat 'npm start'
                }
                echo "App started successfully"
            }
        }
    }
}