pipeline{
    agent any

    tools {
         maven 'maven'
         jdk 'java'
    }

    stages{
        stage('checkout'){
            steps{
                checkout scmGit(branches: [[name: 'master']], extensions: [], userRemoteConfigs: [[credentialsId: 'githubcred', url: 'https://github.com/naveenswathi/java-hello-world-with-maven.git']])
            }
        }
        stage('build'){
            steps{
               sh 'mvn package'
            }
        }
    }
}
