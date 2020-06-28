node('docker'){
    stage("Clone-GIT_Application"){
        git credentialsId: 'varam_github', url: 'https://github.com/Varalakshmi13/studentapp.git'
    }
    stage('Clean compile'){
        sh 'mvn clean compile'

    }
}