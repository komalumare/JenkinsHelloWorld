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
                emailext (
                    subject: "Build Notification",
                    body: "Hello, your build is complete.",
                    to: "te415606@gmail.com",
                    recipientProviders: [[$class: 'DevelopersRecipientProvider']],
                    attachmentsPattern: '**/target/*.jar',
                )
            }
        }
    }
}
