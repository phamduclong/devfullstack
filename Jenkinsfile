pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git branch: 'staging', url: 'https://github.com/phamduclong/devfullstack.git'
            }
        }

        stage('SSH-REMOTE') {
            steps {
                sshPublisher(publishers: [sshPublisherDesc(configName: 'ssh-remote', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: 'cp phamlong.txt duclong.txt', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '', remoteDirectorySDF: false, removePrefix: '', sourceFiles: 'phamlong.txt')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
            }
        }
    }
}