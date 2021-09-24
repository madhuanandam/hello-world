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
        stage('Run maven_job_var_1'){
            steps{
                build job: 'maven_job_var_1'
            }
        }
        stage('install stage'){
            steps{
                sh "mvn clean install package"
            }
        }
        stage('copy the files to docker machine'){
            steps{
                sh 'sudo scp -i /home/ec2-user/devops-madhu-sg.pem /var/lib/jenkins/workspace/Pipeline_for_multiple_stages/webapp/target/webapp.war ec2-user@172.31.3.70:~'
            }
        }
        stage('copy the docker file to docker machine'){
            steps{
                sh 'sudo scp -i /home/ec2-user/devops-madhu-sg.pem /var/lib/jenkins/workspace/Pipeline_for_multiple_stages/Dockerfile ec2-user@172.31.3.70:~'
            }
        }
    }
}
