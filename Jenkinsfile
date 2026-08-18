pipeline {
    agent any

    tools {
        maven 'maven'          
    }

    stages {
        stage('Clone') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/kaye2512/java-hello-world-with-maven.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Run') {
            steps {
                sh 'java -jar target/*.jar'
            }
        }
    }
}
