node {
    stage('checkout_repo'){
       checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/rahul31190/getting-started.git']]]) 
    }
    
    stage('build'){
        
        withCredentials([usernamePassword(credentialsId: 'Git_hub_docker', passwordVariable: 'password', usernameVariable: 'username')]) {
    // some block
    
        }
    
           bat '''@echo off

            set dockerhubrespository=rahul31190/test1
            set username=rahul31190
            set password=Satyam!12

            echo %dockerhubrespository%
            echo %username%
            echo %password%

            docker build -t %dockerhubrespository%:sample .

            docker login -u %username%  -p %password%

            Docker push   %dockerhubrespository%:sample'''


}


}