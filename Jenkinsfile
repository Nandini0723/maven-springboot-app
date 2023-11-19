pipeline {
    agent any
    stages {
        stage("git") {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Nandini0723/maven-springboot-app.git']])
            }
        }
        stage("validate") {
            steps {
                sh "mvn validate"
            }
        }
        stage("freshbuild") {
            steps {
                sh "mvn clean install"
            }
        }
        
    }
}
