pipeline{
    agent any
    tools{
        maven "MAVEN"
        git
    }
    stages{
        stage('build stage'){
            steps{
            sh " echo build"
            }
        }
        stage('another stage'){
            steps{
                sh "echo anotherstage"
            }
        }
    }
}
