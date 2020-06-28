node('docker') {
    stage('Git-clone'){
        git credentialsId: 'varam_github', url: 'https://github.com/Varalakshmi13/studentapp.git'
    }
    stage('packaging'){
        sh 'mvn clean package'
    }
}