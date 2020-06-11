pipeline{
    agent any
    stages{

        stage{'testingWithAWS'}{
            steps{

                sh 'ansible-playbook -C create-ec2.yml'
            }
        }
    }
}