pipeline{
    agent any
    node{
        stage('check if File is good'){
            steps{
                sh 'ansible-playbook -C create-ec2.yml'
            }
        }
        stage('testingWithAWS'){
            steps{
                withAWS(credentials: 'aws-ec2-creation', region: 'us-east-2')
                sh 'ansible-playbook create-ec2.yml'
            }
        }
    }
}