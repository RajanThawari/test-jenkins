pipeline{
    agent{
        node{
           label 'built-in'
           customWorkspace '/media/workspace'
        }
    }
    
    stages{
        stage (git_clone){
            steps{
                git 'https://github.com/RajanThawari/Practice-3.git'
            }
        }
        
        stage (Built){
            steps{
                sh 'cp /media/workspace/index.html /mnt/s3'
            }
        }
        
        stage (Deploy){
            steps{
                sh 'cp /mnt/s3/index.html /var/www/html' 
            }
        }
    }
}
