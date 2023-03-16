pipeline{
    agent any
    
    
    stages{
        stage("git checkout"){
            steps{
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/vinay-k-swift-nav/HelloUniverse']])
            }
        }
        // stage("Build docker image"){
        //     steps{
        //         script{
        //             sh 'docker build -t /hellouniverse-image .'
        //         }
        //     }
        // }
    }
}