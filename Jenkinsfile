pipeline {
    agent any

    stages {
        stage('clone'){
            steps{
                git branch: 'main', url: 'https://github.com/phamduclong/devfullstack.git'
            }
        }
        stage('SSH-AGENT'){
            steps{
                sshagent(['remote-ssh']) {
                    sh 'ssh -o StrictHostKeyChecking=no -l deva_266_wcvn 154.53.61.23 touch pham.txt'
                }
            }
        }
    }
}