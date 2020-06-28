node('docker') {
    stage('Git-clone'){
        git credentialsId: 'varam_github', url: 'https://github.com/Varalakshmi13/studentapp.git'
    }
    stage('packaging'){
        sh 'mvn clean package'
    }
    stage("Deploy to nexus"){
        cp settings.xml ~/.m2/settings.xml
        sh 'mvn deploy -DNEXUS_USERNAME=admin -DNEXUS_PASSWORD=Devops@139'
    }
}