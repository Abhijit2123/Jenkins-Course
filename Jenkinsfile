pipeline {
    agent any
    stages {
        stage("Clean up activity for test"){
            steps {
                deleteDir()
            }
        }
        stage("Clone Repo"){
            steps {
                sh "git clone https://github.com/jenkins-docs/simple-java-maven-app.git"
            }
        }
        stage("Build"){
            steps {
                dir("simple-java-maven-app") {
                    sh "mvn clean install"
                }
            }
        }
        stage("Test"){
            steps {
                dir("simple-java-maven-app") {
                    sh "mvn test"
                }
            }
        }
        stage("End"){
            steps{
                sh "echo 'will miss you singer kk :( :('"
            }
        }
    }
}
