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

        stage('Build') {
            steps {
                sh 'mvn clean deploy'
            }
        }
    }
}
