pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git branch: 'staging', url: 'https://github.com/phamduclong/devfullstack.git'
            }
        }
    }
}