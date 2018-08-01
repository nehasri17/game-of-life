node{
    stage('SCM'){
        git 'https://github.com/nehasri17/game-of-life.git'    
    }
    stage('Build & Package'){
        sh 'mvn package'
    }
    stage('Results'){
        archive 'gameoflife-web/target/gameoflife.war'
    }    
    stage('Reports'){
        junit 'gameoflife-web/target/surefire-reports/*.xml'
    }
}