pipeline{
    agent any
    tools{
        maven "MAVEN3"
        jdk "oraclejdk8"
    }
    environment {
        SNAP REPO = 'vprofile-snapshot'
        NEXUS USER = 'admin'
        NEXUS_PASS = 'admin123'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO 'vpro-maven-central'
        NEXUSIP '172.31.17.187'
        NEXUSPORT = '8081'
        NEXUS_GRP_REPO = 'vpro-maven-group'
        NEXUS_LOGIN = 'nexuslogin'
    }
    stages {
        stage('Build')
        {
            steps{
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}