pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                bat "javac HelloWorld.java"
            }
        }

        stage('Run') {
            steps {
                bat "java HelloWorld"
            }
        }

        stage('Email') {
            steps {
                mail bcc: '', body: 'Build successful', cc: '', from: '', replyTo: '', subject: 'Sample Subject', to: 'te415606@gmail.com'
            }
        }
    }
}
