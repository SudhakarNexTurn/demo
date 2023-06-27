pipeline{
    agent any
    tools{
        maven 'maven3'
        jdk 'jdk17'
    }
    stages{
        stage('clean-workspace'){
            steps{
                cleanWs()
            }   
        }
        stage('checkout'){
            steps{
                echo "Cloning"
                checkout scm
            }
        }
        stage('mvn clean'){
            steps{
               sh 'mvn clean' 
            }
        }
        stage('mvn compile'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('mvn test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('mvn package'){
            steps{
                sh 'mvn package'
            }
        }
        stage('mvn verify'){
            steps{
                sh 'mvn verify'
            }
        }
        stage('mvn install'){
            steps{
                sh 'mvn install'
            }
        }
        }
    }
}
