pipeline{
    agent any
    
    
    stages{
        stage("git checkout"){
            steps{
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/bablooswiftnav/HelloUniverse']])
            }
        }
        stage("Run docker image"){
            steps{
                script{
                    echo 'Hey I am here !!'
                    //  sh 'mount --bind /media/daten/home/hellouniverse /home/hellouniverse'
                    // sh 'docker run  babloojangoo/hello0'
                    sh 'docker run  babloojangoo/hello0'

                    // sh 'docker run -it --home=/ babloojangoo/hellouniverse'
                    // sh 'docker run --mount type=bind,source=/home/hellouniverse,target=/data hellouniverse-image'
                }
            }
        }
    }
}
