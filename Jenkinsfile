pipeline {
    agent any
    tools {
        maven 'Maven3'
        jdk 'Java8'
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }

        stage ('Build') {
            steps {
                sh 'mvn  -f org.javacream.training.jvm/pom.xml install' 
            }
        }
    }
}
