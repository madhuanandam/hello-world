pipeline{
    agent any
    tools{
        maven 'M2_HOME'
        
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
