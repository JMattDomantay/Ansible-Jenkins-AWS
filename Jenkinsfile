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
                withAWS(credentials: 'aws-ec2-creation', region: 'us-east-2')
                sh 'echo $AWS_ACCESS_KEY_ID'
                sh 'echo $AWS_SECRET_ACCESS_KEY'
            }
        }
    }
}