pipeline {
    agent any
    environment {
        PATH = "$PATH:/usr/share/maven/bin"
    }
    stages {
        stage('Clone') {
            steps{
                git branch: 'main', url: 'https://github.com/spring-projects/spring-petclinic'
            }
        }
        stage('Build') {
            steps{
                sh './mvnw package'
            }
        }
    }
}
