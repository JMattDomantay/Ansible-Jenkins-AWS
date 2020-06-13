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
                sh 'ansible-playbook create-ec2.yml'
            }
        }
    }
}