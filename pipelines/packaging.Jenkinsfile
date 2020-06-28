node('docker') {
    stage('Git-clone'){
        git credentialsId: 'varam_github', url: 'https://github.com/Varalakshmi13/studentapp.git'
    }
    stage("package and Deploy to nexus"){  
        withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'nexus_credentials',
        usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD']]) {

                sh '''
                mvn clean
                cp settings.xml ~/.m2/settings.xml
                mvn clean package deploy -DNEXUS_USERNAME=$USERNAME -DNEXUS_PASSWORD=$PASSWORD
                '''
            }
     }
}