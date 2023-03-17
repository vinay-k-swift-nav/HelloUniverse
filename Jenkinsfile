pipeline{
    agent any
    
    
    stages{
        stage("git checkout"){
            steps{
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/vinay-k-swift-nav/HelloUniverse']])
            }
        }
        stage("Build docker image"){
            steps{
                script{
                    echo 'Hey I am here !!'
        //             sh 'mount --bind /media/daten/home/hellouniverse /home/hellouniverse'
                    sh 'docker build -t hellouniverse-image .'
                    sh 'docker run --mount type=bind,source=/home/hellouniverse,target=/data hellouniverse-image'
                }
            }
        }
    }
}