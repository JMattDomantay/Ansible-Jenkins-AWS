pipeline{
    agent any
    stages{
        stage('check if File is good'){
            steps{
                sh 'ansible-playbook -C create-ec2.yml'
            }
        }
        stage('testingWithAWS'){
            steps{
                withCredentials([usernamePassword(credentialsId: 'aws-ec2-creation', accessKeyVariable: 'AWS_ACCESS_KEY_ID', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY')]) {
                sh 'echo $AWS_ACCESS_KEY_ID'
                sh 'echo $AWS_SECRET_ACCESS_KEY'
                }
            }
        }
    }
}