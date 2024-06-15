pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                bat "javac HelloWorld.java"
            }
        stage('Run') {
            steps {
                bat "java HelloWorld"
            }
        }
    }
}
