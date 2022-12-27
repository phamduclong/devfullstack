pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git branch: 'staging', url: 'https://github.com/phamduclong/devfullstack.git'
            }
        }

        def remote = [:]
        remote.name = 'ssh-remote'
        remote.host = '154.53.61.23'
        remote.user = 'deva_266_wcvn'
        remote.password = 'jej0HWSURp9g5CLk'
        remote.allowAnyHosts = true
        stage('Remote SSH') {
            sshCommand remote: remote, command: "cd www/devapp.wp.edu.vn/devfullstack"
            sshCommand remote: remote, command: "git pull origin staging"
        }
    }
}