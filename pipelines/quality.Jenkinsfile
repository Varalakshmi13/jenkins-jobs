node('docker'){
    stage("Clone-GIT_Application"){
        git credentialsId: 'varam_github', url: 'https://github.com/Varalakshmi13/studentapp.git'
    }
    stage('Code-quality'){
         sh 'mvn clean compile sonar:sonar -Dsonar.projectKey=studentapp   -Dsonar.host.url=http://172.31.78.93:9000   -Dsonar.login=28369e7a1feb33af5681b604b20dbf791321a0c4'
    }
}