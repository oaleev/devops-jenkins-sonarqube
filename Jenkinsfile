pipeline {
    agent any
    environment {
        SONARQUBE_HOSTNAME=tool 'sonar'
        GRADLE_HOME=tool 'gradle'
    }
    stages {
        stage('Prep') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/raleev/devops_webapp.git']])
            }
        }
        stage('build') {
          steps {
            sh "${GRADLE_HOME}/bin/gradle build"
          }
        }
    }
}
