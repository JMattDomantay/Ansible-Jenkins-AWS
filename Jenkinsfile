pipeline{
    agent any
    stages{

        stage('testingWithAWS'){
            steps{
                withAWS(credentials: 'aws-ec2-creation', region: 'us-east-2')
                sh 'ansible-playbook create-ec2.yml'
            }
        }
    }
}