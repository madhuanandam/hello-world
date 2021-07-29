pipeline{
    agent any
    tools{
        maven "maven"
        git
    }
    stages{
        stage('compile stage'){
            steps{
            sh "mvn clean compile"
            }
        }
        stage('test stage'){
            steps{
                sh "mvn test"
            }

        }
        stage('deploy stage'){
            steps{
                sh "mvn deploy"
            }
        }
    }
}
