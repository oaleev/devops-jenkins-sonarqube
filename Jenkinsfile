pipeline {
    agent any
    env {
        SONARQUBE_HOSTNAME = 'sonarqube'
        GRADLE_HOME = tool name: 'gradle', type: 'hudson.plugins.gradle.GradleInstallation'
    }
    stages {
        stage('Prep') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/raleev/devops_webapp.git']])
            }
        }
    }
}
