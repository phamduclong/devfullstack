pipeline {
    agent any

    stages {
        stage('clone'){
            steps{
                git branch: 'main', url: 'https://github.com/phamduclong/devfullstack.git'
            }
        }
    }
}