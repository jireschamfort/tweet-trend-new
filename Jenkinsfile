pipeline {
    agent {
        label 'mavennode'
    }

    stages {
        stage('clone repos int') {
            steps {
                git branch: 'main', url: 'https://github.com/jireschamfort/tweet-trend-new.git'
            }
        }
environment {
    PATH = "$PATH:/opt/apache-maven-3.9.6/bin"
}
        stage('Build') {
            steps {
                sh 'mvn clean deploy'
            }
        }
    }
}
