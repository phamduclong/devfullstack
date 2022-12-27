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
                sshPublisher(publishers: [sshPublisherDesc(configName: 'dev', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: 'echo "buiding"', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '/var/www/deva_266_wcvn/data/www/devapp.wp.edu.vn', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '/var/jenkins_home/workspace/devfullstack-pipeline')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
            }
        }
    }
}