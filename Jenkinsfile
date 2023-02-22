pipeline{
    agent{
        node{
           label 'built-in'
           customWorkspace '/mnt/pipeline2'
        }
    }
    
    stages{
        stage (git_clone){
            steps{
                git 'https://github.com/RajanThawari/game-of-life.git'
            }
        }
        
        stage (Built){
            steps{
                sh 'mvn install -DskipTests'
            }
        }
        
        stage (Deploy){
            steps{
                sh 'cp /mnt/pipeline2/gameoflife-web/target/gameoflife.war /mnt/data/apache-tomcat-9.0.71/webapps' 
            }
        }
    }
}
